FROM ubuntu:14.04.2

MAINTAINER Wei Zeng

RUN apt-get update && \
    apt-get install -y --force-yes ruby && \
    apt-get clean && rm -rf /tmp/* && \
    gem install bundler

ADD clickme /root/clickme

RUN cd /root/clickme && bundle install

EXPOSE 4567

WORKDIR /root/clickme

CMD bundle exec ruby ./clickme.rb


