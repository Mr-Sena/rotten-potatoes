FROM python:3.11.5
WORKDIR /source
COPY requirements.txt ./
RUN python -m pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]