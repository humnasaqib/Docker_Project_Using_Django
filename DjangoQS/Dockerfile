FROM ubuntu

WORKDIR /app/DjangoQS

COPY requirements.txt /app/DjangoQS/requirements.txt
COPY myproject /app/DjangoQS/myproject

# Install dependencies, including libpq-dev
RUN apt-get update && \
    apt-get install -y python3 python3-pip libpq-dev && \
    pip install -r /app/DjangoQS/requirements.txt

# Set the working directory to the inner DjangoQS folder
WORKDIR /app/DjangoQS/myproject

# Specify the CMD instruction
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]
