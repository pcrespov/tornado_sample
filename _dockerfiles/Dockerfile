FROM ubuntu:16.04

# https://packages.ubuntu.com/
# TODO: build-dep fails!
RUN  apt-get update -qq \
  && apt-get -y -qq upgrade \
  && apt-get install -yq \
    python-dev \
    python-pip
#\&& apt-get build-dep -y python-dev

WORKDIR /home/usr
COPY sample/requirements.txt .
RUN pip install -r requirements.txt

COPY sample .

CMD ["python", "app.py", "--port=8888"]
