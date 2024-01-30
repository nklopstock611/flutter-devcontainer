FROM ubuntu:latest

RUN apt-get update && \
    apt-get install -y curl git unzip xz-utils libglu1-mesa openjdk-11-jdk

# Instala Flutter y Dart
RUN git clone https://github.com/flutter/flutter.git /flutter && \
    /flutter/bin/flutter --version

ENV PATH="/flutter/bin:${PATH}"

# Configura el SDK de Flutter
RUN flutter config --no-analytics && \
    flutter precache && \
    flutter doctor --android-licenses

WORKDIR /workspace
