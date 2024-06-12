FROM ruby:3.3.1-slim
RUN apt-get update -qq

# Minimal requirements to run a Rails app
RUN apt-get update && apt-get install -qq -y --no-install-recommends \
      build-essential \
      libpq-dev \
      tzdata 

ENV APP_NAME /app
RUN mkdir /$APP_NAME
WORKDIR /$APP_NAME

COPY Gemfile* $APP_NAME/

ENV BUNDLE_PATH=/bundle \
    BUNDLE_JOBS=3 \
    BUNDLE_BIN=/bundle/bin \
    GEM_HOME=/bundle
ENV PATH="${BUNDLE_BIN}:${PATH}"
RUN bundle install

COPY . /$APP_NAME

EXPOSE 3000
