ARG BUILD_FROM
FROM ${BUILD_FROM}

RUN apk add --no-cache git python3 py3-pip

RUN python3 -m venv /opt/venv
ENV PATH="/opt/venv/bin:${PATH}"

RUN pip install git+https://github.com/rohitmanokaran/wyoming-stt-api.git

COPY run.sh /
RUN chmod a+x /run.sh

CMD ["/run.sh"]
