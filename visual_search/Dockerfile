FROM python:2.7.14-jessie

MAINTAINER yangboz "z@smartkit.info"

RUN apt-get update && apt-get install -y build-essential git wget
RUN apt-get install -y vim


COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt

RUN ls
WORKDIR /app/lib
RUN make
#Preprocess SGFs
ENTRYPOINT ["python]
EXPOSE 5001
CMD ["server.py"]
