FROM nginx:alpine

COPY nginx.vue.conf /etc/nginx/conf.d/nginx.vue.conf
RUN mkdir -p /usr/local/nginx/html
COPY dist /usr/share/nginx/html
RUN chown -R nginx:nginx /usr/share/nginx/html

EXPOSE 8083
ENTRYPOINT nginx -g 'daemon off;' 
