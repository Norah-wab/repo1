FROM python:stretch
WORKDIR /app
RUN pip install --upgrade pip
COPY requirements.txt /app
COPY main.py /app
RUN pip install -r requirements.txt
ENTRYPOINT ["gunicorn", "-b", ":8080", "main:APP"]
