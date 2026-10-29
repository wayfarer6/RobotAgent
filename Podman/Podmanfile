FROM ubuntu:24.04
ENV DEBIAN_FRONTEND=noninteractive
ENV DISPLAY=:1

RUN apt-get update && apt-get install -y \
    ubuntu-desktop-minimal \
    tightvncserver \
    novnc \
    websockify \
    net-tools \
    curl \
    git \
    && apt-get clean \
    && rm -rf /var/lib/lists/*

RUN mkdir -p ~/.vnc && \
    echo "password" | vncpasswd -f > ~/.vnc/passwd && \
    chmod 600 ~/.vnc/passwd

RUN echo '#!/bin/sh\n\
vncserver :1 -geometry 1920x1080 -depth 24\n\
/usr/share/novnc/utils/launch.sh --vnc localhost:5901 --listen 8080\n\
' > /entrypoint.sh && chmod +x /entrypoint.sh

EXPOSE 8080 5901

CMD ["/entrypoint.sh"]
