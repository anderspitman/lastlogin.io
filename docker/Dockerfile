FROM alpine:3.18

RUN apk add --no-cache curl ca-certificates fuse3 sqlite

VOLUME ["/data"]

VOLUME ["/api"]

EXPOSE 1616

ENTRYPOINT ["litefs", "mount"]

COPY --from=flyio/litefs:0.5 /usr/local/bin/litefs /usr/local/bin/litefs

COPY ./IP2LOCATION-LITE-DB3.IPV6.BIN /

COPY ./litefs.yml /etc/
COPY ./obligator /obligator/obligator
COPY ./static static
