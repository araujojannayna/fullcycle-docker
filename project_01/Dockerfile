FROM golang:1.18 AS builder
COPY . /build/
WORKDIR /build
RUN go build -o ./out/go-sample-app .

FROM scratch
COPY --from=builder /build .
WORKDIR /build
ENTRYPOINT ["/out/go-sample-app"]