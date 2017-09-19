FROM redis:3.2.10

RUN mkdir /opt/redis && \
    mkdir /var/log/redis && \
    mkdir /opt/sentinel

ADD config/master.conf /opt/redis/redis.conf
ADD config/sentinel.conf /opt/sentinel/sentinel.conf

RUN chown -R redis.redis /opt/redis && \
    chown -R redis.redis /var/log/redis && \
    chown -R redis.redis /opt/sentinel

#USER redis

CMD [ "redis-server", "/opt/redis/redis.conf" ]
