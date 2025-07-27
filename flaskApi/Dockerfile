FROM python:3.9-slim

EXPOSE 5002

WORKDIR /app
COPY . /app

#Install curl for testing
RUN apt-get update && apt-get install -y curl
COPY X_test.csv ./app

# Install pip requirements
COPY requirements.txt ./app
RUN python -m pip install -r requirements.txt

# Entry point
CMD ["gunicorn", "--bind", "0.0.0.0:5002", "app:app"]
