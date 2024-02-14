FROM python:3.9.11

ENV PYTHONUNBUFFERED 1

RUN mkdir -p /home/workspace/src

# 作成したディレクトリを表示して確認
RUN ls -la /home

COPY containers/requirements.txt /home/workspace/
COPY src /home/workspace/src

# 作成したディレクトリを表示して確認
RUN ls -la /home/workspace/

# 作成したディレクトリを表示して確認
RUN ls -la /home/workspace/src

# 作成したディレクトリを表示して確認
RUN ls -la /home/workspace/src/qumcum-api/qumcum_web/qumcum_app

WORKDIR /home/workspace

RUN pip install --upgrade pip \
    && pip install --upgrade setuptools \
    && pip install -r requirements.txt

CMD ["python", "src/qumcum-api/qumcum_web/qumcum_app/manage.py", "runserver", "0.0.0.0:8000"]
