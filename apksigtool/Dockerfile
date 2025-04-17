# use python image
FROM python:alpine

# install git
RUN apk add git

# set working directory
WORKDIR /app

# clone apksigtool
RUN git clone https://github.com/obfusk/apksigtool.git
RUN pip install -e apksigtool

# run apksigtool
ENTRYPOINT ["apksigtool"]
