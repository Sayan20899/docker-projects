FROM python:3.12-slim

# Set the working directory
WORKDIR /app

# Copy the requirements file
COPY requirements.txt /app/

# Create a virtual environment inside the container
RUN python3 -m venv /env

# Activate the virtual environment and install dependencies
RUN /env/bin/pip install --upgrade pip && /env/bin/pip install -r requirements.txt

# Copy the rest of the project files
COPY . /app

# Expose the port
EXPOSE 5000

# Run the application
CMD ["/env/bin/python", "app.py"]
