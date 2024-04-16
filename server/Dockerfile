
FROM ubuntu:20.04 AS builder

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends cmake build-essential

ADD . /source/
WORKDIR /build/
RUN cmake -B . -S /source
RUN cmake --build .

FROM ubuntu:20.04

ENV SERVER 1
WORKDIR /server
COPY --from=builder /build/natserver /server/natserver

ENTRYPOINT /server/natserver -v ${SERVER}