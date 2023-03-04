# ZeroDoor
# Cross-Platform Backdoors Generator
# docker build -t zeroDoor .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python-pip git-core && \
  cd /opt

RUN git clone https://github.com/YAHYA950/Zerodoor.git

COPY start.sh /start.sh

RUN \
  apt remove -y git-core && \
  apt clean && \
  apt autoremove -y && \
  chmod 775 /start.sh

ENTRYPOINT ["/start.sh"]

