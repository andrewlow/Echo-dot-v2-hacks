# syntax=docker/dockerfile:1
FROM python:3

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
  apt-get update -qq && apt-get install -y adb fastboot git

RUN git clone https://github.com/Dragon863/EchoCLI.git ./EchoCLI
RUN git clone https://github.com/bkerler/mtkclient.git ./mtkclient

WORKDIR /mtkclient
RUN pip install -r requirements.txt

WORKDIR /EchoCLI
RUN pip install -r requirements.txt

CMD [ "/bin/bash" ]
