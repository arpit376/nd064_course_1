# Use a Python base image in version 3.8
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install the dependencies specified in the requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose the application port 3111
EXPOSE 3111

# Ensure the database is initialized with the pre-defined posts
RUN python init_db.py

# Command to run the application
CMD ["python", "app.py"]
