FROM ruby:2.7
MAINTAINER mordonez

LABEL org.label-schema.name="Ruby with nodejs" \
      org.label-schema.description="Docker container with ruby" \
      org.label-schema.vendor="mordonez" \
      org.label-schema.license="MIT" \
      org.label-schema.url="https://hub.docker.com/r/microsoft/mlopspython" \
      org.label-schema.schema-version="1.0"

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
      nodejs ssh sshpass rsync

RUN curl https://www.npmjs.com/install.sh | sh

# throw errors if Gemfile has been modified since Gemfile.lock
RUN bundle config --global frozen 1

WORKDIR /usr/src/app

CMD [ "/usr/src/app" ]
