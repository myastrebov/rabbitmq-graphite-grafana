FROM registry.k.avito.ru/avito/rabbitmq:3.6.6
MAINTAINER Maxposter <development@maxposter.ru>

# set timezone
RUN echo Europe/Moscow | tee /etc/timezone && rm -f /etc/localtime && dpkg-reconfigure --frontend noninteractive tzdata

COPY ./plugins/rabbitmq_delayed_message_exchange-0.0.1.ez /usr/lib/rabbitmq/lib/rabbitmq_server-3.6.6/plugins/rabbitmq_delayed_message_exchange-0.0.1.ez
RUN rabbitmq-plugins enable rabbitmq_delayed_message_exchange && rabbitmq-plugins enable rabbitmq_web_stomp && rabbitmq-plugins enable rabbitmq_management

# Expose port for web stomp
EXPOSE 15671
