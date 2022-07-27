FROM ruby:3.1.2

ENV APP_ROOT /api

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir $APP_ROOT

WORKDIR $APP_ROOT

ADD Gemfile $APP_ROOT/Gemfile
ADD Gemfile.lock $APP_ROOT/Gemfile.lock

RUN gem update --system --no-document \
  && gem install bundler --no-document -v 2.3.15
RUN bundle config set path 'vendor/bundle' \
  && bundle install --jobs 4 --retry 3

ADD . /api
