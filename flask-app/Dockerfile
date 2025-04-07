FROM python:3.11
WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt  # Sử dụng --no-cache-dir để tránh cache package
RUN pip list  # Kiểm tra phiên bản đã cài
COPY app.py ./
EXPOSE 5000
CMD ["python", "app.py"]