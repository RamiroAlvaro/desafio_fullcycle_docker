FROM golang:1.16 AS builder

WORKDIR /app

COPY . .

RUN go build -o fullcycle fullcycle.go

FROM scratch

COPY --from=builder /app .

CMD ["./fullcycle"]