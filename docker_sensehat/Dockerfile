FROM arm64v8/ubuntu

WORKDIR /tmp

RUN apt-get update && apt-get install -y curl python3 librtimulib7 git libopenjp2-7 python3-distutils python3-apt build-essential sense-hat nano

ADD ./sensehat.py /home/
ADD ./datapoints/myfile.csv /data/myfile.csv
RUN rm -f /tmp/*.deb
RUN apt-get clean

WORKDIR /

CMD ["python3", "/home/sensehat.py"]
