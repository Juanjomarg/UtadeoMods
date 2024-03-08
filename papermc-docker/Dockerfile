FROM alpine:latest

# Environment variables
# https://papermc.io/downloads/all
ENV MC_VERSION="" \
    PAPER_BUILD="" \
    EULA="true" \
    MC_RAM="" \
    JAVA_OPTS=""

COPY papermc.sh .
RUN apk update \
    && apk add openjdk17-jre \
    && apk add bash \
    && apk add wget \
    && apk add jq \
    && mkdir ./papermc

# Start script
CMD ["bash", "/papermc.sh"]

# Container setup
EXPOSE 25565/tcp
EXPOSE 25565/udp
