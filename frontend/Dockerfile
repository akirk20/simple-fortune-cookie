FROM golang:1.19-alpine

WORKDIR /app

COPY go.mod ./
RUN go mod download && go mod verify

COPY . .
RUN go build -v -o /usr/local/bin/app ./...

EXPOSE 8080

CMD ["app"]
