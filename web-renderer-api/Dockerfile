ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

RUN apk add --update nodejs nodejs-npm

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

RUN cd url-to-pdf-api  \
&&  npm install

COPY env url-to-pdf-api/.env

CMD [ "/run.sh" ]