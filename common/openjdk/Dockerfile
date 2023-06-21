FROM openjdk:8-jre-alpine
ENV TZ=Asia/Shanghai
MAINTAINER 287737281@qq.com

RUN mkdir /app
WORKDIR /app
COPY target/testCase.jar /app/testCase.jar

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories
# RUN apk update && apk add --update ttf-dejavu fontconfig

ENTRYPOINT [ "java", "-jar",  "/app/testCase.jar" ]