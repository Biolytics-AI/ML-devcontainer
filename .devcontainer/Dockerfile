FROM pytorch/pytorch:2.2.1-cuda12.1-cudnn8-runtime
RUN apt-get update && apt-get install -yqq ca-certificates curl
RUN apt-get update && apt-get install -y build-essential libffi-dev libssl-dev gcc \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
# install poetry
RUN pip install --no-cache-dir poetry==1.8.2

ENV POETRY_NO_INTERACTION=1 \
    POETRY_VIRTUALENVS_IN_PROJECT=1 \
    POETRY_VIRTUALENVS_CREATE=1 \
    POETRY_CACHE_DIR=/tmp/poetry_cache
