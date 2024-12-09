# Use an official Python runtime as a parent image
FROM python:3.10-slim

# Set the working directory
WORKDIR /app

# Install dependencies
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the project code
COPY . /app/

# Expose the application port
EXPOSE 8000

# Command to run the Django application
CMD ["gunicorn", "todoapi.wsgi:application", "--bind", "0.0.0.0:8000"]
