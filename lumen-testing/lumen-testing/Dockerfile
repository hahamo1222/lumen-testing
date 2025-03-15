# 使用 Python 3.10 作为基础镜像
FROM python:3.10

# 设置工作目录
WORKDIR /app

# 复制依赖文件（确保 requirements.txt 存在）
COPY requirements.txt .

# 升级 pip 并安装依赖
RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt

# 复制所有项目文件
COPY . .

# 运行 FastAPI 服务器
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]