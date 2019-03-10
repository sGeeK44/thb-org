FROM python:3.6-stretch

RUN \
    apt-get -y update \
    && apt install -y postgresql-client \
    && rm -rf /var/lib/apt/lists/*

RUN \
    pip install --upgrade pip \
    && pip install -U setuptools

ENV DJANGO_ROOT_APP_DIR /home/src
WORKDIR $DJANGO_ROOT_APP_DIR

# Install pip requirements.
ARG REQUIREMENTS=common.txt
COPY requirements $DJANGO_ROOT_APP_DIR/requirements
RUN pip install -r requirements/$REQUIREMENTS

COPY . $DJANGO_ROOT_APP_DIR

EXPOSE 8000

CMD ["bash"]
