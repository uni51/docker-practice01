FROM nginx:1.12.2
ENV LANG ja_JP.UTF-8
RUN apt-get update -qq && apt-get install -y apt-utils locales && sed -i -e 's/# ja_JP.UTF-8/ja_JP.UTF-8/g' /etc/locale.gen && locale-gen ja_JP.UTF-8
ENV LC_TIME C
ADD ./containers/nginx/nginx.conf /etc/nginx/nginx.conf
ADD ./containers/nginx/default.conf /etc/nginx/conf.d/default.conf
