## My expirements on Airflow 


## Airflow Installation and Setup
- mkdir airflow-expirements
- curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.7.3/docker-compose.yaml'
- mkdir -p ./dags ./logs ./plugins ./config

- echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env
- docker-compose up airflow-init
- docker-compose up -d

// localhost:8080

---
### Using:
- Redis as broker
- Postgresql as metadata DB
- Celery as a queue in airflow-scheduler
- Flask in airflow-webserver