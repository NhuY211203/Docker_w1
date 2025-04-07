FROM golang:1.20
WORKDIR /app
COPY main.go ./
RUN go build -o myapp
EXPOSE 8080
CMD ["./myapp"]