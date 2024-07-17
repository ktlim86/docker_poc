FROM debian:12.6

RUN apt-get update

RUN apt install python3 python3-pip build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev wget -y

RUN pip3 config set global.break-system-packages true

RUN pip3 install apache-airflow

RUN mkdir -p /opt/airflow/dags

RUN mkdir /opt/airflow/plugins

RUN mkdir /opt/airflow/logs

RUN addgroup --gid 1000 airflow

RUN useradd -d /home/airflow airflow -g airflow -ms /bin/bash

RUN chgrp -R airflow /opt/airflow

RUN chmod -R g+w /opt/airflow

USER airflow

CMD ["echo","'hello world!'"]