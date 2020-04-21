FROM ubuntu:18.04

RUN apt update && apt install -y conntrack netcat
COPY ./wait-for /wait-for
COPY ./start /start
RUN chmod +x /start /wait-for

#ENTRYPOINT ["/bin/sh", "-c", "'while true; do /wait-for http://goflow:8080/metrics -- conntrack -D -p udp; done'"] 
ENTRYPOINT ["/start"]