FROM python:3.9

# Set the working directory
WORKDIR /app

# Install system dependencies, including OpenSSL
RUN apt-get update && apt-get install -y libssl-dev

# Copy your application files
COPY . .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the correct port for Streamlit
EXPOSE 8501

# Run the Streamlit app
CMD ["streamlit", "run", "cicd.py", "--server.port=8501", "--server.address=0.0.0.0"]
