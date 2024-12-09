# Use an official Python runtime as a parent image
FROM python:3.10-slim

# Set the working directory
WORKDIR /app

# Install Ansible and dependencies
RUN pip install --no-cache-dir ansible

# Install additional dependencies from requirements.txt
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the project code
COPY . /app/

# Expose the application port
EXPOSE 8000

# Command to run the Django application (you can change this later if you want to run ansible-playbook)
CMD ["gunicorn", "todoapi.wsgi:application", "--bind", "0.0.0.0:8000"]
