FROM python:3.7.8

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y --no-install-recommends cmake # for xlearn install && \
    apt-get install -y git && apt-get clean
RUN pip install --upgrade pip && \
    pip install poetry

RUN mkdir -p /root/.ssh

WORKDIR /app
# COPY pyproject.toml poetry.lock ./
# RUN poetry install
COPY requirements.txt ./
RUN pip install -r requirements.txt
