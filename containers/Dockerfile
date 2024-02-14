FROM python:3.9.11

ENV PYTHONUNBUFFERED 1

RUN mkdir -p /home/workspace
COPY /containers/requirements.txt /home/workspace/
COPY /src /home/workspace
WORKDIR /home/workspace

RUN pip install --upgrade pip\
    && pip install --upgrade setuptools\
    && pip install -r requirements.txt
    
CMD ["python", "/src/manage.py", "runserver", "0.0.0.0:8000"]
