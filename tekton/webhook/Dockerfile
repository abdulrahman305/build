FROM python:3.14.0a3-alpine

WORKDIR /app

ADD requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

ADD ./*.py /app

ENV PORT 5000
CMD ["gunicorn", "app:app", "--config=config.py"]
