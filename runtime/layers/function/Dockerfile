ARG LAYER_IMAGE
FROM $LAYER_IMAGE

WORKDIR /opt

COPY bootstrap bootstrap
COPY php.ini bref/etc/php/conf.d/bref.ini

FROM lambci/lambda:provided

WORKDIR /
COPY --from=0  /opt /opt
RUN pwd
WORKDIR /var/task
