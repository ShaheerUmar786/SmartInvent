FROM python:3.9-slim-buster

WORKDIR /app

COPY erp_backend/requirements.txt .
RUN apt-get update && apt-get install -y pkg-config libmariadb-dev gcc
RUN pip install -r requirements.txt

COPY . .

CMD ["python", "erp_backend/manage.py", "runserver", "0.0.0.0:8000"]