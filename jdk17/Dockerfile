FROM ghcr.io/graalvm/graalvm-ce:ol7-java17

RUN yum install -y unzip zip
RUN  curl -s "https://get.sdkman.io" | bash; \
        source "$HOME/.sdkman/bin/sdkman-init.sh"; \
        sdk install gradle && \
        gu install native-image

RUN source "$HOME/.sdkman/bin/sdkman-init.sh"
ENV GRADLE_HOME=/root/.sdkman/candidates/gradle/current
ENV PATH=$PATH:$GRADLE_HOME/bin
RUN gradle --version