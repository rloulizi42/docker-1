FROM debian

RUN apt-get update -y && apt-get upgrade -y && \
	apt-get install bzip2 wget -y && \
	wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 && \
	bunzip2 *.bz2 && \
	tar -xvf *.tar

EXPOSE 9987/udp 10011 30033

CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]
