#
#
#--------------------------------------------------------------------------
# node 14-pm2
#--------------------------------------------------------------------------
#

FROM chinayin/node:14-slim
LABEL maintainer="chinayin <whereismoney@qq.com>"

ENV NODE_VERSION 14.17.3

USER root
RUN set -eux; \
    # Install pm2
    npm install pm2 -g; \
    \
    pm2 -version

USER node
EXPOSE 3000 43554
CMD ["pm2-runtime", "start", "pm2.json"]
