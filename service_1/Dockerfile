FROM golang:1.20

WORKDIR /app
COPY . .
RUN go mod init service1
RUN go build -o app

EXPOSE 8001
CMD ["./app"]
