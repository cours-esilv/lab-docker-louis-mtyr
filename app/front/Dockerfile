FROM nginx

WORKDIR /usr/share/nginx/html

COPY . /front

ENV WS_BACK_URL=<back-end URL>

EXPOSE 5000

ENTRYPOINT ["sh", "-c", "envsubst < /usr/share/nginx/html/config.template.js > /usr/share/nginx/html/config.js && nginx -g 'daemon off;'"]