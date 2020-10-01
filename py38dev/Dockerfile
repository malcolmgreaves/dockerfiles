FROM python:3.8-slim

# References
# - https://stackoverflow.com/a/54763270/362021
ENV POETRY_VERSION 1.1.0rc1
ENV PYTHONFAULTHANDLER=1
ENV PYTHONUNBUFFERED=1
ENV PYTHONHASHSEED=random
ENV PIP_NO_CACHE_DIR=off
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
ENV PIP_DEFAULT_TIMEOUT=100

RUN apt-get -qq update && apt-get upgrade -y && apt-get install -y \
    build-essential \
    curl \
    dumb-init \
    git \
    wget \
    vim \
    libspatialindex-dev

# Python project uses poetry
RUN curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/${POETRY_VERSION}/get-poetry.py | python
ENV PATH="${PATH}:/root/.poetry/bin"
