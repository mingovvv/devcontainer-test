FROM mcr.microsoft.com/devcontainers/java:1-17-bullseye

ARG INSTALL_MAVEN="false"
ARG MAVEN_VERSION="3.9.2"

ARG INSTALL_GRADLE="true"
ARG GRADLE_VERSION="8.2"

# Maven 설치 (설치 옵션이 true일 때)
RUN if [ "${INSTALL_MAVEN}" = "true" ]; then \
      su vscode -c "umask 0002 && . /usr/local/sdkman/bin/sdkman-init.sh && sdk install maven \"${MAVEN_VERSION}\""; \
    else \
      echo 'Skipping Maven installation'; \
    fi

# Gradle 설치 (설치 옵션이 true일 때)
RUN if [ "${INSTALL_GRADLE}" = "true" ]; then \
      su vscode -c "umask 0002 && . /usr/local/sdkman/bin/sdkman-init.sh && sdk install gradle \"${GRADLE_VERSION}\""; \
    else \
      echo 'Skipping Gradle installation'; \
    fi