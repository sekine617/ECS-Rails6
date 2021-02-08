FROM ruby:2.6.3

RUN apt-get update -qq && \
  apt-get install -y apt-utils \
  build-essential \
  libpq-dev \
  nodejs \
  vim \
  default-mysql-client 

WORKDIR /app

ADD Gemfile .
ADD Gemfile.lock .
RUN bundle install -j4
RUN gem install bundler:2.1.4
RUN bundle install

ADD . /app


EXPOSE 3000

