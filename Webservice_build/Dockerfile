FROM python:3.9.12-slim

RUN pip install pipenv

WORKDIR /app
COPY ["Pipfile","Pipfile.lock","./"]

RUN pipenv install --system --deploy --ignore-pipfile

COPY ["adoption_predict.py", "adoption_prediction.bin", "./"]

EXPOSE 9999

ENTRYPOINT ["gunicorn", "--bind=0.0.0.0:9999", "adoption_predict:app"]