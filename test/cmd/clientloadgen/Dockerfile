FROM golang:1.10.3 as builder
WORKDIR /go/src/github.com/GoogleCloudPlatform/open-match/test/cmd/clientloadgen/
COPY ./ ./
RUN go get -d -v 
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o clientloadgen . 

CMD ["./clientloadgen"]
