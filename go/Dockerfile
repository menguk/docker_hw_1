FROM golang:1.13.5-alpine
COPY main.go .
RUN go build ./main.go

FROM alpine:3.10.3
COPY --from=0 /go/main .
EXPOSE 8080
CMD ["./main"]