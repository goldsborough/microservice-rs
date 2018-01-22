FROM rustlang/rust:nightly
MAINTAINER <peter@goldsborough.me>

ENV SSL_CERT_FILE=/etc/ssl/certs/ca-certificates.crt

# Install vim for in-place editing.
RUN apt-get update -y && apt-get install -y vim

WORKDIR /var/www/microservice/
COPY . .

RUN rustc --version
RUN cargo install

CMD ["microservice"]
