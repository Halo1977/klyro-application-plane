# docker/services/Dockerfile

FROM python:3.9-slim

ENV PYTHONUNBUFFERED=1

WORKDIR /app

COPY ./services/requirements /requirements
RUN pip install --no-cache-dir -r /requirements/base.txt

COPY ./services /app

EXPOSE 8001

CMD ["python", "manage.py", "runserver", "0.0.0.0:8001"]
