FROM python:3.11

WORKDIR /khootclone

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt


COPY . .

RUN  python manage.py makemigrations

RUN python manage.py migrate

CMD ["python","manage.py","runserver"]