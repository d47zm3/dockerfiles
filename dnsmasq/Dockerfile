FROM alpine
LABEL maintainer="d47zm3@gmail.com"
RUN apk update && apk --no-cache add dnsmasq
RUN mkdir -p /etc/default/
RUN echo -e "ENABLED=1\nIGNORE_RESOLVCONF=yes" > /etc/default/dnsmasq
COPY dnsmasq.conf /etc/dnsmasq.conf
ENTRYPOINT ["dnsmasq","--no-daemon"]
