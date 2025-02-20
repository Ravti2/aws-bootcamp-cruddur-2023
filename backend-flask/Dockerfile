FROM python:3.10-slim-buster
# Inside Container
# make a new folder inside container
WORKDIR /backend-flask

#Outside container->Inside container
#this contains libraries we want install to run the app
COPY requirements.txt requirements.txt

#Inside container
#intall the python libraries used for the app
RUN pip3 install -r requirements.txt

#Outside container->Inside container
#. means everything in the current directory
# first period .-/backend flask (outside container)
# second period .-/backend flask (inside container)
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD
#
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]