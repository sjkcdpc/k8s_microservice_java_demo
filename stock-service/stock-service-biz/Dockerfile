FROM hub.hulai.com/java:8-jdk-alpine

LABEL Maintainer="madscdpc@gmail.com" \
      Description="Java"

ENV JAVA_OPTS="$JAVA_OPTS -Dfile.encoding=UTF8 -Duser.timezone=GMT+08"

RUN sed -i.bak 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories && \
    apk add -U tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

COPY ./target/stock-service-biz.jar ./

COPY pinpoint /pinpoint

EXPOSE 8030

CMD java -jar -javaagent:/pinpoint/pinpoint-bootstrap-1.8.3.jar \
              -Dpinpoint.agentId=${HOSTNAME} \
              -Dpinpoint.applicationName=ms-stock $JAVA_OPTS /stock-service-biz.jar
