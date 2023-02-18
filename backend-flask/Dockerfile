FROM python:3.10-slim-buster

#make a new folder inside container
WORKDIR /backend-flask

#copy requirements from outside to inside container folder and run 
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
#copy everything from outside to inside container
COPY . .
#set envars
# set inside container
ENV FLASK_ENV=development

EXPOSE ${PORT}

#command to run flask
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]