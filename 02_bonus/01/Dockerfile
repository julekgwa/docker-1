FROM ubuntu

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install curl -y && apt-get install apt-transport-https -y

# installing nvm (node veriosn manager)
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash

ENV NVM_DIR=~/.nvm

RUN [ "/bin/bash" , "-c", "source ~/.nvm/nvm.sh && echo 'source ~/.nvm/nvm.sh' >> ~/.bashrc" ]

# installing node
RUN curl -sL https://deb.nodesource.com/setup_7.x | bash -
RUN apt-get install nodejs -y

# configure yarn repository
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

# installing yarn
RUN apt-get update -y && apt-get install yarn -y

# installing tools
RUN apt-get install vim -y && apt-get install git -y

EXPOSE 8080

CMD [ "bin/bash" ]