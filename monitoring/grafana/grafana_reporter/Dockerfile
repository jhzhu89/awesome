FROM golang:1.17-alpine as builder
WORKDIR /home
RUN apk --no-cache add git
RUN go install -v github.com/IzakMarais/reporter/cmd/grafana-reporter@latest

FROM ivanpondal/alpine-latex:2.0.1
COPY --from=builder /go/bin/grafana-reporter /usr/bin/grafana-reporter

USER root
ENTRYPOINT ["grafana-reporter"]
