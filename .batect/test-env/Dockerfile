FROM docker:20.10.3-dind@sha256:7e1f7ea149d1d23e739dd763e918aa8adab341cef04e0ede6b9487c1859e445e

RUN apk add --no-cache \
    bash=5.1.0-r0 \
    curl=7.74.0-r0 \
    openjdk11-jre-headless=11.0.9_p11-r1 \
    python3=3.8.7-r0

COPY entrypoint.sh /usr/local/bin/

ENV DOCKER_HOST=unix:///var/run/docker.sock
ENV DOCKER_TLS_CERTDIR=""

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
