FROM python:3.10

RUN apt-get update
RUN apt-get install ffmpeg libsm6 libxext6  -y

WORKDIR /back_end

COPY back_end/requirements.txt .
RUN pip install --upgrade pip
RUN pip3 install --no-cache-dir -r requirements.txt

COPY back_end .

COPY common /back_end/app/common

EXPOSE 8296

ENTRYPOINT ["gunicorn", "--log-level", "INFO", "-b", ":8296", "-t", "120", "run:APP"]
