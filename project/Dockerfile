# Use the official Python base image in version 3.8
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Copy the application code into the container
COPY techtrends/ .

# Install the dependencies
RUN pip install -r requirements.txt

# Expose the application port
EXPOSE 3111

# Initialize the database with pre-defined posts
RUN python init_db.py

# Command to run the application
CMD ["python", "app.py"]