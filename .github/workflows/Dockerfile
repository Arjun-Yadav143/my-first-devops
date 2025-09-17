# Dockerfile (place at repo root)
FROM python:3.10-slim

# Create and switch to /app (WORKDIR will create it automatically)
WORKDIR /app

# Copy only requirements first for layer caching
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Create extra directories inside the image
RUN mkdir -p /app/logs /app/data

# Copy remaining project files into /app
COPY . .

# Default command to run your app
CMD ["python", "app.py"]

