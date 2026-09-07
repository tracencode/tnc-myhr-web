FROM nginx:1.27-alpine

# Official nginx image runs envsubst on templates using $PORT from Render.
COPY nginx.conf.template /etc/nginx/templates/default.conf.template
COPY . /usr/share/nginx/html

# Don't serve the nginx template as a static file.
RUN rm -f /usr/share/nginx/html/nginx.conf.template \
    && rm -f /usr/share/nginx/html/Dockerfile

ENV PORT=8080
EXPOSE 8080
