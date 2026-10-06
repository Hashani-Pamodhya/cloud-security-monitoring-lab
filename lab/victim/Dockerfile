FROM ubuntu:24.04
RUN apt-get update && apt-get install -y openssh-server rsyslog sudo \
    && rm -rf /var/lib/apt/lists/* \
    && mkdir -p /run/sshd \
    && useradd -m -s /bin/bash testuser \
    && echo 'testuser:sunshine1' | chpasswd
CMD ["bash", "-c", "rsyslogd && /usr/sbin/sshd -D"]
