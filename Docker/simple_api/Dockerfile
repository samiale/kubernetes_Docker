FROM python:2.7-stretch

#Maintainer of image
LABEL maintainer="285893@supinfo.com"

#Install of dependencies
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv

COPY student_age.py /

COPY ./student_age.json /data/

VOLUME ["/data"]

EXPOSE 5000

CMD [ "python", "./student_age.py" ]
