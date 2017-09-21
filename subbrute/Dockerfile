FROM alpine:latest
LABEL maintainer "James Abley <james.abley@gmail.com>"

RUN buildDeps=' \
		ca-certificates \
		openssl \
	' \
	&& apk --no-cache add --update \
	python3 \
	$buildDeps \
	&& pip3 install dnspython \
	&& wget https://github.com/TheRook/subbrute/archive/77.tar.gz \
	&& tar xzf 77.tar.gz \
	&& apk del --purge $buildDeps

ENTRYPOINT ["python3", "./subbrute-77/subbrute.py"]
