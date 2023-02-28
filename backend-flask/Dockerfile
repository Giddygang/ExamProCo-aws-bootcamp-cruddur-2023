FROM python:3.10-slim-buster

# Inside Container
# Make a new folder inside the Container
WORKDIR /backend-flask 

# Outside Container -> Inside Container
# This Contains the libraries needed to run the App
COPY requirements.txt requirements.txt

# Inside Container
# Installs the python libraries used to run the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
COPY . .

#Set Environment Variables
# Inside the Container and will remain set when the Container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# Python3 -m flask run --host=0.0.0.0 --port=4567
# -m == module, shortcut to run flask 
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]