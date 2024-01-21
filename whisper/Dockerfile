FROM python:3.11.7-bullseye

# Install Whisper
WORKDIR /usr/src
ARG WHISPER_VERSION='1.0.1'

RUN \
    git clone https://github.com/xiaozhch5/wyoming-faster-whisper \
    && cd wyoming-faster-whisper \
    && python3 setup.py install

WORKDIR /
COPY run.sh ./

EXPOSE 10300

ENTRYPOINT ["bash", "/run.sh"]
