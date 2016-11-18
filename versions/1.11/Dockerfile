# AWS-CLI v1.11
# docker run --rm takatakato/awscli --version
# docker run --rm -v $HOME/.aws:/root/.aws takatakato/awscli iam list-users

FROM takatakato/python:2.7

RUN apk --no-cache add --virtual build-dependencies py-pip \
      && apk --no-cache add groff jq \
      && pip install 'awscli == 1.11.15' \
      && apk del --purge build-dependencies

VOLUME /root/.aws

ENTRYPOINT ["aws"]
CMD ["--version"]