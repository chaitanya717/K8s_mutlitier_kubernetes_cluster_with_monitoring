FROM python:3

# Install system dependencies
RUN apt-get update && apt-get install -y \
    libpq-dev \
    gcc \
    python3-dev

# Copy app
COPY . /app

WORKDIR /app

# Install Python dependencies
RUN pip install -r requirements.txt

# Expose port 5000
EXPOSE 5000

# Run the server when the container is launched
CMD ["python", "app.py"]
