# Example Dockerfile for whisper-transcriber
FROM python:3.10-slim
WORKDIR /app
COPY package.json yarn.lock ./
RUN apt-get update && apt-get install -y nodejs npm && npm install -g yarn \
    && yarn install --production
COPY . .
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root"]
