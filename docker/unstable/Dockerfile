FROM docker.io/library/python:3.12.6-slim@sha256:8ac54da5710cdd31639bb66f5bc1888948fc2866c0b5b52913b4b33d8252e510

# This file is generated from docker:unstable in Taskfile.yml
COPY var/requirements.txt /var/tmp/build/

RUN \
    pip install -r /var/tmp/build/requirements.txt

COPY dist/*.whl /var/tmp/build/

RUN \
    pip install --no-deps /var/tmp/build/*.whl && \
    rdfpipe --version

ENTRYPOINT [ ]
