FROM python:3.6-stretch

RUN \
    apt-get -y update \
    && apt install -y postgresql-client \
    && rm -rf /var/lib/apt/lists/*

RUN \
    pip install --upgrade pip \
    && pip install -U setuptools

COPY . /home/src

EXPOSE 8000

CMD ["bash"]
