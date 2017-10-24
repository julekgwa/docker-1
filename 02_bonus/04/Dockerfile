FROM debian

RUN apt-get -y update && apt-get -y upgrade && apt-get -y install git && apt-get -y install wget gcc

RUN mkdir -p /home/dev/local
WORKDIR /home/dev
RUN wget https://storage.googleapis.com/golang/go1.9.1.linux-amd64.tar.gz && tar -C /home/dev/local -xvzf go1.9.1.linux-amd64.tar.gz \
    && rm -rf go1.9.1.linux-amd64.tar.gz
    
ENV GOROOT=/home/dev/local/go
ENV GOPATH=/home/dev/go
ENV PATH=$PATH:$GOROOT/bin:$GOPATH/bin

CMD [ "/bin/bash" ]