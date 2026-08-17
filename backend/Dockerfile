FROM python:3.9-slim

# Working directory inside the container
WORKDIR /app

# Copy all files from current dir to container's working dir
COPY . .

# Install dependencies from the requirements file
RUN pip install --no-cache-dir -r requirements.txt

# Command to start the flask application with 4 worker processes on port 7860
CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:7860", "app:superkart_api"]
