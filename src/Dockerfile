FROM debian:12
LABEL maintainer="viclaune@study.com"
RUN apt-get update && apt-get install nginx curl -y && rm -rf /var/lib/apt/lists/*
EXPOSE 80 
ENV APP_VERSION 1.0.0
ENTRYPOINT [ "nginx" ]
CMD ["-g", "daemon off;"]
HEALTHCHECK --timeout=3s --retries=2 CMD curl -f localhost || exit 1