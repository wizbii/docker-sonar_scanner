FROM openjdk:10

ARG NODEJS_VERSION=8

ENV SONAR_SCANNER_VERSION "3.2.0.1227"
ENV SONAR_SCANNER_NAME "sonar-scanner-cli-$SONAR_SCANNER_VERSION"
ENV SONAR_SCANNER_FOLDER_NAME "sonar-scanner-$SONAR_SCANNER_VERSION"

WORKDIR /sonar-scanner

RUN curl -sL https://deb.nodesource.com/setup_$NODEJS_VERSION.x | bash - && \
    apt-get update && apt-get install -y unzip wget nodejs && \
    wget https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/$SONAR_SCANNER_NAME.zip && \
    unzip $SONAR_SCANNER_NAME.zip

ENV PATH $PATH:/sonar-scanner/$SONAR_SCANNER_FOLDER_NAME/bin
