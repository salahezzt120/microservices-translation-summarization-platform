# Use the official Python slim image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file and install dependencies
COPY ar2en_service/requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY ar2en_service/ ./ar2en_service

# Expose the default port for FastAPI
EXPOSE 8000

# Command to run the app
CMD ["uvicorn", "ar2en_service.main:app", "--host", "0.0.0.0", "--port", "8000"]
