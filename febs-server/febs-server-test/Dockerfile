FROM openjdk:8u212-jre
MAINTAINER MrBird 852252810@qq.com

COPY ./target/febs-server-test-2.2-RELEASE.jar /febs/febs-server-test-2.2-RELEASE.jar
ADD ./agent/skywalking-agent.jar /agent/

ENTRYPOINT ["java", "-javaagent:/agent/skywalking-agent.jar", "-Dskywalking.agent.service_name=febs-server-test", "-Dskywalking.collector.backend_service=skywalkingIp:11800", "-jar", "/febs/febs-server-test-2.2-RELEASE.jar"]