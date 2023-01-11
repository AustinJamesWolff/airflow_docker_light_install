# airflow_docker_light_install
### A light installation of Airflow on Docker for local MacOS use.

This repo contains a lightweight airflow-docker compose file, specifically for
MacOS with limited resources that cannot run the docker-compose recommended by
the official Apache Airflow website.

You can get started by following these commands:

1. Download the file
```
curl -LfO "https://github.com/AustinJamesWolff/airflow_docker_light_install/blob/main/docker-compose.yaml"
```

2. Make the necessary directories:
```
mkdir ./logs ./dags ./plugins
```

3. Define the environment variables we need for the local environment:
```
echo -e "AIRFLOW_UID=$(id -u)" > .env
echo -e "AIRFLOW_GID=0" >> .env
```

4. Initialize Airflow:
```
docker-compose up airflow-init
```

5. Start and run the containers:
```
docker-compose up
```

6. Yo ushould be able to visit localhost:8080 and sign into the Airflow UI with the username and password: airflow
