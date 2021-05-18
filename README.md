# README #

## Steps to reproduce
Clone project, create virtualenv and install dependency

```bash
# Create virtual environment
python3 -m venv env

source env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

Run project, redis, celery beat, celery

```bash
./manage.py runserver
docker-compose up
celery -A settings beat
celery - A settings worker -l INFO --pool=solo
```
