FROM python:2-alpine

LABEL Maintainer="thoba@sanbi.ac.za"

RUN apk --update add git openssh gcc musl-dev build-base openssl-dev \
    libffi-dev libxslt-dev libxml2-dev python-dev && \
    rm -rf /var/lib/apt/lists/* && \
    rm /var/cache/apk/*

RUN pip install pandas

COPY requirements.txt .

RUN pip install -r requirements.txt
