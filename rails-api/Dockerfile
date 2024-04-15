FROM ruby:2.6.7

WORKDIR /rails-api

COPY Gemfile Gemfile.lock ./
RUN mkdir -p log && touch log/development.log

RUN gem install bundler -v 2.3.9

RUN bundle install

RUN gem install foreman

# Start the main process.
CMD ["foreman", "start", "-f", "Procfile"]
