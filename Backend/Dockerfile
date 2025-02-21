# Use official Python 3.9 image
FROM python:3.9

# Set working directory inside the container
WORKDIR /app

# Set environment variables to prevent Python from writing .pyc files and buffer issues
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Upgrade pip to avoid dependency conflicts
RUN pip install --upgrade pip

# Copy requirements file and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy backend source code
COPY . .

# Expose backend API port
EXPOSE 5000

# Start the Flask app
CMD ["python", "app.py"]
