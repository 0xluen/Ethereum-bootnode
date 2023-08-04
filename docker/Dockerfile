FROM ubuntu:latest
RUN apt-get update && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update && \
    apt-get install -y bootnode
RUN bootnode --genkey /root/core.key
EXPOSE 30301/udp
ENTRYPOINT ["bootnode", "--nodekey=/root/core.key", "--verbosity=4", "--addr=165.232.119.113:30301"]
