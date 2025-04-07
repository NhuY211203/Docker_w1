# Stage 1: Build
FROM node:18 AS builder
WORKDIR /app

# Copy package.json vào container
COPY package.json ./

# Cài đặt dependencies
RUN npm install

# Copy mã nguồn vào container
COPY app.js ./

# Không cần `RUN npm run build` vì app này không có bước build

# Stage 2: Run
FROM node:18-alpine
WORKDIR /app

# Copy từ stage build sang container mới
COPY --from=builder /app ./

# Expose cổng 3000
EXPOSE 3000

# Chạy ứng dụng
CMD ["node", "app.js"]
