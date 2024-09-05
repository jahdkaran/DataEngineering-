FROM python:3.12-slim-bookworm


RUN apt update && apt install -y wget curl gnupg2 ca-certificates lsb-release && apt clean && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# Install libraries needed for data science and data engineering sql
RUN pip install numpy pandas matplotlib seaborn scikit-learn jupyter psycopg2-binary sqlalchemy bs4 requests lxml 

EXPOSE 8888

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root", "--no-browser"]