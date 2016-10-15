## BUILDING
##   (from project root directory)
##   $ docker build -t python-for-gordsellar-hexenbracken .
##
## RUNNING
##   $ docker run python-for-gordsellar-hexenbracken

FROM gcr.io/stacksmith-images/ubuntu-buildpack:14.04-r10

MAINTAINER Bitnami <containers@bitnami.com>

ENV STACKSMITH_STACK_ID="8jxoafw" \
    STACKSMITH_STACK_NAME="Python for gordsellar/hexenbracken" \
    STACKSMITH_STACK_PRIVATE="1"

RUN bitnami-pkg install python-3.5.2-1 --checksum 6347e5d0c2e318d9bf25a927dc6762bd8a6e490bfab06179179545fa9d3e0d3c

ENV PATH=/opt/bitnami/python/bin:$PATH

## STACKSMITH-END: Modifications below this line will be unchanged when regenerating

# Python base template
COPY . /app
WORKDIR /app

RUN pip install -r requirements.txt

CMD ["python"]
