FROM hyperledger/besu:latest

COPY data.zip /home/besu/
RUN ls -ali /home/besu
RUN apt-get install -y unzip
RUN unzip -uo /home/besu/data.zip -d /home/besu
