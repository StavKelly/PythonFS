FROM python:3.11-slim

RUN groupadd -r seetrue && useradd -r -g seetrue seetrue

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY main.py .

RUN chown -R seetrue:seetrue /app
USER seetrue

CMD ["python3", "main.py"]
