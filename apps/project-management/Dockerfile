FROM node:14.15.0-alpine as install-stage
WORKDIR /app
COPY ./dist/apps/project-management .

FROM nginx:stable-alpine as production-stage
COPY --from=install-stage /app /usr/share/nginx/html
EXPOSE 80

