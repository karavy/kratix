# Add Dockerfile contents here
FROM "mikefarah/yq:4"
RUN [ "mkdir", "/tmp/transfer" ]

ADD cnpg-instance.yaml /tmp/transfer/cnpg-instance.yaml
ADD execute-pipeline execute-pipeline

CMD [ "sh", "-c", "./execute-pipeline"]
ENTRYPOINT []
