FROM alpine:latest

RUN	apk update \
	&& apk add sniproxy

COPY overlay/ /

EXPOSE 443

CMD [ "sniproxy", "-f", "-c", "/etc/sniproxy.conf" ]
