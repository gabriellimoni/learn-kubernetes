FROM oven/bun:1

WORKDIR /usr/src/app

COPY ./ ./

EXPOSE 4000

RUN bun install

CMD [ "bun", "run", "/usr/src/app/index.js" ]
