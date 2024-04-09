FROM alpine:3.19
RUN apk update && apk add --no-cache openssl
COPY entrypoint /
WORKDIR /work
ENTRYPOINT ["/entrypoint"]
