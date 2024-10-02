FROM apache/airflow:slim-2.4.1-python3.8

USER root

ARG DEV_APT_DEPS="\
     apt-transport-https \
     apt-utils \
     build-essential \
     ca-certificates \
     cron \
     curl \
     gnupg \
     gnupg2 \
     dirmngr \
     freetds-bin \
     freetds-dev \
     git \
     gosu \
     krb5-user \
     ldap-utils \
     libffi-dev \
     libkrb5-dev \
     libldap2-dev \
     libpq-dev \
     libsasl2-2 \
     libsasl2-dev \
     libsasl2-modules \
     libssl-dev \
     libtasn1-6 \
     libxml2 \
     locales  \
     lsb-release \
     openssh-client \
     openssl \
     postgresql-client \
     sasl2-bin \
     software-properties-common \
     sqlite3 \
     sudo \
     unixodbc \
     unixodbc-dev \
     yarn"

USER airflow

RUN pip install --no-cache-dir 'setuptools==65.5.1'
RUN pip install --no-cache-dir 'wheel==0.38.1'
RUN pip install --no-cache-dir 'Authlib==0.15.5'
RUN pip install --no-cache-dir 'Werkzeug==2.1.2'
RUN pip install --no-cache-dir 'redis==3.5.3'
RUN pip install --no-cache-dir 'psycopg2-binary==2.9.3'
#RUN pip install --no-cache-dir 'psycopg2==2.9.3'
RUN pip install --no-cache-dir 'click==8.0.4'
RUN pip install --no-cache-dir 'celery-flower==1.0.1'
RUN pip install --no-cache-dir 'certifi==2022.12.7'
RUN pip install --no-cache-dir 'cryptography==39.0.2'
RUN pip install --no-cache-dir 'databricks-cli==0.14.3'
RUN pip install --no-cache-dir 'markdown-it-py==2.2.0'
RUN pip install --no-cache-dir 'oyaml==0.9'
RUN pip install --no-cache-dir 'python-dotenv==0.14.0'
RUN pip install --no-cache-dir 'pyyaml==6.0'
RUN pip install --no-cache-dir 'ruamel.yaml==0.17.21'
RUN pip install --no-cache-dir 'snowflake-connector-python==3.0.2'
RUN pip install --no-cache-dir 'snowflake-sqlalchemy==1.4.7'
RUN pip install --no-cache-dir 'azure-core==1.24.1'
RUN pip install --no-cache-dir 'azure-identity==1.12.0'
RUN pip install --no-cache-dir 'azure-keyvault==4.1.0'
RUN pip install --no-cache-dir 'apache-airflow-providers-databricks==4.0.0'
RUN pip install --no-cache-dir 'apache-airflow-providers-snowflake==4.0.4'
RUN pip install --no-cache-dir 'apache-airflow-providers-common-sql==1.3.4'
RUN pip install --no-cache-dir 'apache-airflow[async]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow[celery]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow[cgroups]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow[pandas]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow[password]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow[rabbitmq]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow[virtualenv]==2.4.1'
RUN pip install --no-cache-dir 'apache-airflow-providers-microsoft-azure==5.2.1'
RUN pip install --no-cache-dir 'kubernetes==26.1.0'
RUN pip install --no-cache-dir 'apache-airflow-providers-cncf-kubernetes==5.2.0'
RUN pip install --no-cache-dir 'statsd==4.0.1'
RUN pip install --no-cache-dir 'azure-storage-blob==12.15.0'
#RUN pip install --no-cache-dir -r requirements.txt
# RUN pip install --no-cache-dir 'apache-airflow-backport-providers-email==2020.6.24'
# RUN pip install --no-cache-dir 'airflow[statsd]'
# RUN pip install --no-cache-dir 'airflow[smtp]'
# RUN pip install --no-cache-dir 'apache-airflow-providers-ssh==3.4.0'
# RUN pip install --no-cache-dir 'pip install apache-airflow-providers-postgres==5.4.0'

RUN rm /home/airflow/.local/lib/python3.8/site-packages/gevent/tests/test_server.key \
  && rm /home/airflow/.local/lib/python3.8/site-packages/tornado/test/test.key \
  && rm /home/airflow/.local/lib/python3.8/site-packages/gevent/tests/2_7_keycert.pem \
  && rm /home/airflow/.local/lib/python3.8/site-packages/gevent/tests/server.key \
  && rm /home/airflow/.local/lib/python3.8/site-packages/gevent/tests/wrongcert.pem \
  && rm /home/airflow/.local/lib/python3.8/site-packages/gevent/tests/keycert.pem \
  && rm /home/airflow/.local/lib/python3.8/site-packages/gevent/tests/badcert.pem \
  && rm /home/airflow/.local/lib/python3.8/site-packages/flower/static/js/jquery-1.7.2.min.js

# RUN rm -rf /home/airflow/.local/lib/python3.8/site-packages/airflow

