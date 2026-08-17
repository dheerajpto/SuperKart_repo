FROM python:3.9-slim

WORKDIR /app

COPY . .

# Install dependencies from the requirements file
RUN pip3 install -r requirements.txt

# Command to start the flask application with 4 worker processes on port 7860
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0", "--server.enableXsrfProtection=false"]
