FROM python:3.12.9-bullseye

WORKDIR /home/work

# Coppy requirements.txt file and install required libraries
COPY requirements.txt /home/work/
RUN pip install -r requirements.txt

# Copy all necessary files from directory on PC to the container
COPY main.py /home/work/

EXPOSE 5000

CMD [ "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "5000" ]