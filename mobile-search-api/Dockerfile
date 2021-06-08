FROM openjdk:8-jdk-alpine
RUN mkdir app
ADD target/mobile-search-api-0.0.1-SNAPSHOT.jar /app/
WORKDIR app
EXPOSE 8899
CMD ["java","-jar","mobile-search-api-0.0.1-SNAPSHOT.jar"]