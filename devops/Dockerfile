ARG python_version=3.10
FROM python:${python_version} as BASE

RUN apt-get install python3-ledger
RUN pip install -r src/requirements.txt

ENTRYPOINT [ "gunicorn", "-w", "1", "-b", "0.0.0.0:8080", "src.app:app" ]
