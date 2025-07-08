# Add Dockerfile contents here
FROM "ubuntu:24.04"

RUN apt update && apt install -y wget gh
RUN wget -qO /usr/local/bin/yq https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 && \
    chmod a+x /usr/local/bin/yq
RUN apt install -y git

RUN [ "mkdir", "/tmp/transfer" ]

ADD cnpg-instance.yaml /tmp/transfer/cnpg-instance.yaml
ADD execute-pipeline execute-pipeline

CMD [ "sh", "-c", "./execute-pipeline"]
ENTRYPOINT []
