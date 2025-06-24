FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy code
COPY . .

# Install uv
RUN pip install uv

# Create virtual environment and install dependencies
RUN uv venv && uv pip install flask

# Expose the port
EXPOSE 8002

# Run the app
CMD ["uv", "run", "app.py"]

