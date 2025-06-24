# Stage 1: Build the Go binary statically
FROM golang:1.20 AS builder

WORKDIR /app
COPY . .

# Build with static linking flags
RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o service1 main.go

# Stage 2: Run with lightweight Alpine
FROM alpine:latest

WORKDIR /root/
COPY --from=builder /app/service1 .

EXPOSE 8001
CMD ["./service1"]

