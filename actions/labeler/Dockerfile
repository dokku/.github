FROM alpine:3.10.3
WORKDIR /app

RUN apk --no-cache add unzip
ADD https://github.com/tonglil/labeler/releases/download/1.0.0/labeler-linux-amd64.zip /tmp/labeler.zip
RUN unzip -d /bin/ /tmp/labeler.zip
COPY entrypoint /bin/entrypoint
COPY labels.yml /app/labels.yml

ENTRYPOINT ["/bin/entrypoint"]
