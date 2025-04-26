FROM python:3.11-slim
# Set environment variables
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1# 
#Set the working directory inside the container
WORKDIR /flask-app
# Copy only requirements first to leverage Docker cache
COPY requirements.txt .
# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt
# Copy the rest of the application code
COPY . .
# Expose the port Flask runs on
EXPOSE 9200
# Command to run the app
CMD ["python", "app.py"]