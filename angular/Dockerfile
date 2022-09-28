FROM node:14-alpine3.12 as builder

RUN mkdir /app
WORKDIR /app

COPY holiday_requests/package.json holiday_requests/package-lock.json /app/holiday_requests/

RUN npm install --prefix holiday_requests

COPY . /app

RUN npm run build --prefix holiday_requests -- --output-path=./dist/out


FROM nginx:1.20.1-alpine

RUN rm -rf /usr/share/nginx/html/*

COPY --from=builder /app/holiday_requests/dist/out /usr/share/nginx/html

COPY ./nginx.conf /etc/nginx/conf.d/default.conf
