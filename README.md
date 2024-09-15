# Dockerized-Monitoring-Stack-with-Prometheus-and-Grafana

This project sets up a simple monitoring stack using Docker, Prometheus, and Grafana. It includes an Nginx server as the target for monitoring. The stack is orchestrated using Docker Compose to facilitate easy setup and management.

## File setup

First, I create the docker-compose.yml file which includes the configuration for the Nginx server, the Nginx Exporter and Prometheus. In the same directory, I create the prometheus.yml which tells Prometheus to scrape the Nginx Exporter running at nginx-exporter:9113. I do not include Grafana as I have already installed it locally on my Ubuntu 24.04 machine. Then I run Docker Compose.

## Check server and metrics

I open the browser and head to the appropriate addresses in order to check that:

- The Nginx server is running
  
![Screenshot (367)](https://github.com/user-attachments/assets/280f9860-09f2-4566-bf6e-aded6b8dc324)
  
- The Nginx Exporter is exposing Nginx metrics

![Screenshot (368)](https://github.com/user-attachments/assets/930d6ccb-8741-4a4b-bebb-7c39d052456f)

- Prometheus is scraping the Nginx Exporter

![Screenshot (369)](https://github.com/user-attachments/assets/41aebff1-5f4d-4d62-b69d-6171fead0002)

Finally in Grafana I set up the metrics I want to query in my dashboard and view the final outcome.

![Screenshot (370)](https://github.com/user-attachments/assets/66a4cce0-a15c-4d9b-ae80-7c97d2453051)

![Screenshot (371)](https://github.com/user-attachments/assets/4f8fca5a-d030-46e0-8e07-de3bedcbf415)
