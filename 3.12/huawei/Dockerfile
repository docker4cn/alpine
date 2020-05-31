FROM alpine:3.12

ENV TZ='Asia/Shanghai'
RUN apk add --no-cache \
        tzdata \
        ca-certificates \
    && sed -i "s@http://dl-cdn.alpinelinux.org@https://mirrors.huaweicloud.com@g" /etc/apk/repositories

COPY ./context/huawei/ /root/
