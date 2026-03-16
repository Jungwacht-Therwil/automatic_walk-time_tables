FROM cypress/included:15.12.0

WORKDIR /opt

RUN apt update
RUN apt install -y unzip

COPY package.json .
COPY package-lock.json .
RUN npm ci

WORKDIR /opt/e2e
RUN npx cypress verify
