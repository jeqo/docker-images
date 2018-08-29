FROM openjdk:8-jre-alpine

ENV	JMX_EXPORTER_HTTP_PORT=5556

EXPOSE ${JMX_EXPORTER_HTTP_PORT}

RUN mkdir /jmx-exporter

WORKDIR /jmx-exporter

ADD jmx_prometheus_httpserver-0.3.1-jar-with-dependencies.jar jmx_prometheus_httpserver.jar
ADD httpserver.yml config/httpserver.yml

#    -Dcom.sun.management.jmxremote.port=5555 \
#    -Dcom.sun.management.jmxremote.ssl=false \
#    -Dcom.sun.management.jmxremote.authenticate=false \
CMD java \
    -jar \
    jmx_prometheus_httpserver.jar \
    ${JMX_EXPORTER_HTTP_PORT} \
    config/httpserver.yml
