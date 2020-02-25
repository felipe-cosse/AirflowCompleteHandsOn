# AirflowCompleteHandsOn
Curso de Airflow da Udemy - The Complete Hands-On Introduction to Apache Airflow

Link: https://www.udemy.com/course/the-complete-hands-on-course-to-master-apache-airflow/


ssh -p 2200 airflow@localhost

sudo -E ./start.sh

Role/App - Login - Password

root root centos

user airflow airflow

mysql root mysql

mysql hive hive

rabbitmq admin rabbit


App - URL

Spark master http://localhost:8081

Kibana http://localhost:5601

Airflow http://localhost:8080

RabbitMQ http://localhost:15672

source .sandbox/bin/activate

pip install "apache-airflow[celery, crypto, postgres, rabbitmq, redir]==1.10.6"

pip install --upgrade Flask

airflow initdb

cd airflow

ls

grep dags_folder airflow.cfg

mkdir dags

vim airflow.cfg

/load_examples

locad_examples = False

:wq!

airflow initdb

airflow resetdb

cp ../airflow_files/hello_world.py dags/


airflow scheduler

airflow webserver


rm -rf airflow.db

airflow initdb

sqlite3 airflow.db

.tables (Control-D)

airflow resetdb


airflow list_dags

airflow list_tasks hello_world_dag

airflow list_tasks hello_world_dag --tree

airflow test hello_world_dag python_task 2019-01-01

airflow -h

cp airflow_files/twitter_dag_v_1.py airflow/dags/

vim dags/twitter_dag_v_1.py

vim airflow_files/fetching_tweet.py

vim airflow_files/cleaning_tweet.py

cp airflow_files/twitter_dag_v_1.py airflow/dags/twitter_dag_v_2.py

ls /tmp/

hadoop fs -ls /tmp/

hive

SHOW TABLES;

SELECT COUNT(*) FROM tweets;

cp airflow_files/data/data.csv airflow_files/

grep worker_refresh_interval airflow/airflow.cfg

grep dag_dir_list_interval airflow/airflow.cfg

cp airflow_files/simple_dag_backfill.py airflow/dags/

vim airflow/dags/simple_dag_backfill.py

date



