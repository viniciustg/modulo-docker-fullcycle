# Build stage
FROM golang:1.16-alpine as builder

WORKDIR /app

COPY . .

RUN go build -o hello hello.go

# Run stage

FROM scratch

COPY --from=builder /app .

CMD ["./hello"]

