FROM alpine:3.3
RUN apk --no-cache add -t deps wget ca-certificates \
  && wget -q -O - https://github.com/papertrail/remote_syslog2/releases/download/v0.17/remote_syslog_linux_amd64.tar.gz \
  | tar -zxf - \
  && apk del deps
ENTRYPOINT ["/remote_syslog/remote_syslog", "-D"]
ADD log_files.yml /etc/log_files.yml
