FROM openjdk:8u111-jdk-alpine

ENV SERVICE_NAME holamundo

RUN addgroup --gid 30020 $SERVICE_NAME && \
	adduser --home /app --system --shell /sbin/nologin --uid 30020 $SERVICE_NAME
	


RUN chown -R $SERVICE_NAME
EXPOSE 8081

USER $SERVICE_NAME
WORKDIR /app

COPY ../../../target/hello-0.0.1-SNAPSHOT.jar /app

CMD ["java","-jar","hello-0.0.1-SNAPSHOT.jar"]