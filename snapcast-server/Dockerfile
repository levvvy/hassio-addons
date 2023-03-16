ARG BUILD_FROM
FROM $BUILD_FROM

# Add repository information
ARG VERSION
LABEL org.opencontainers.image.source https://github.com/levvvy/hassio-addons/snapcast-server
LABEL org.opencontainers.image.version=$VERSION

# Set shell
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Install snapserver
RUN apk add --no-cache snapcast-server

# Copy data
COPY run.sh /
RUN chmod a+x /run.sh

# Expose Snapcast Server port
EXPOSE 1704

CMD [ "/run.sh" ]
