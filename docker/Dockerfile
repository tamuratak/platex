FROM texlive/texlive:latest
ENV DEBIAN_FRONTEND=noninteractive
RUN apt -y update && apt -y upgrade
RUN apt -y install imagemagick nodejs npm
RUN npm install -g reg-cli
RUN mkdir /home/app
RUN apt -y install git
RUN mkdir /home/platex_dev
WORKDIR /home/platex_dev
COPY .. .
RUN make && make install && fmtutil-sys --byfmt platex-dev
