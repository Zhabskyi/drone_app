FROM golang:1.12

WORKDIR /code/

ADD . ./

ENV GO111MODULE=on

RUN go mod tidy
RUN go build -o ./drone_server
RUN export PAATH=$PATH:/code/drone_server

CMD ["drone_server"]