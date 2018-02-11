FROM Debian

RUN apt-get update -y && \
    apt-get install rails -y && \
    apt-get install nodejs -y

ONBUILD COPY . /opt/app

ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install \
    rails db:migrate \
    rails db:seed
