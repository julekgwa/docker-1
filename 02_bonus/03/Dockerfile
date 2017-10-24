FROM debian

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install gcc -y && apt-get install make -y && apt-get install git -y \
    && apt-get install vim -y

WORKDIR /app

CMD [ "/bin/bash" ]