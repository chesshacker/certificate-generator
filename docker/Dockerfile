FROM alpine
RUN apk update && apk add --no-cache openssl
COPY entrypoint /
WORKDIR /work
ENTRYPOINT ["/entrypoint"]
