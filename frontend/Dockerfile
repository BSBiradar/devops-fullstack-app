FROM amazonlinux:2
LABEL author=biradar

RUN yum install -y \
    curl \
    && curl -sL https://rpm.nodesource.com/setup_14.x | bash - \
    && yum install -y nodejs

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 3000
CMD ["npm", "start"]