FROM ubuntu
RUN apt-get update -y
RUN apt-get install -y curl 
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -E -
RUN apt install -y nodejs 
WORKDIR /home
COPY . server
COPY ./run.sh ./run.sh
WORKDIR /home/server 
RUN npm i  
RUN npm run build
WORKDIR /home
ENTRYPOINT ["run.sh"]
EXPOSE 80