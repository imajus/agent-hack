FROM python:3.10.15

RUN apt-get update && apt-get install --yes --no-install-recommends make

WORKDIR /app

COPY requirements-dev.txt .
RUN pip install -r requirements-dev.txt
COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

ENV GEMINI_API_KEY=
ENV CDP_API_KEY_NAME=
ENV CDP_API_KEY_PRIVATE_KEY=
ENV NETWORK_ID=
ENV GRAPH_API_KEY=

EXPOSE 5000

CMD ["make", "start-prod"]
