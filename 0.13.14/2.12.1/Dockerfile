# Generated automatically by update.sh
# Do no edit this file

FROM bigtruedata/scala:2.12.1

# Install build dependencies
RUN apk add --no-cache --virtual=.dependencies tar wget

RUN wget -O- "http://dl.bintray.com/sbt/native-packages/sbt/0.13.14/sbt-0.13.14.tgz" \
    |  tar xzf - -C /usr/local --strip-components=1 \
    && sbt exit

# Remove build dependencies
RUN apk del --no-cache .dependencies

VOLUME /app
WORKDIR /app

CMD ["sbt"]
