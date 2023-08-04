apt-get update && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update && \
    apt-get install -y bootnode

bootnode --nodekey=/root/core.key --verbosity=4 --addr=0.0.0.0:30301
