FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Install filesender package
RUN pip install --upgrade pip
RUN pip install --no-cache-dir filesender-client

# Set environment variables
ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

# Create a non-root user to run the application
RUN useradd -m appuser
USER appuser

# Command to run when container starts
ENTRYPOINT ["filesender"]