# Apache Unomi Docker Starter
![Kibana](Screenshot%202025-06-20%20121344.png)
![Unomi](Screenshot%202025-06-20%20121358.png)
![Swagger UI](Screenshot%202025-06-20%20121415.png)
A complete, ready-to-use Docker Compose setup for running Apache Unomi. This repository includes Unomi, Elasticsearch for data storage, and Kibana for data visualization.

## Included Services

-   **Apache Unomi**: The Customer Data Platform server.
-   **Elasticsearch**: The backend database required by Unomi.
-   **Kibana**: A web UI to explore the data stored in Elasticsearch.

## Prerequisites

-   [Docker](https://docs.docker.com/get-docker/)
-   [Docker Compose](https://docs.docker.com/compose/install/)

## How to Run

1.  **Clone the repository** (or just create the `docker-compose.yml` file).
2.  **Start the services:**
    ```bash
    docker-compose up -d
    ```
    Please be patient on the first run, as Docker needs to download the images and Elasticsearch needs some time to initialize.

## Accessing Services

Once the containers are up and running, you can access the services at the following URLs:

-   **Apache Unomi API**: `http://localhost:8181`
-   **Kibana Web UI**: `http://localhost:5601`
-   **Elasticsearch API**: `http://localhost:9200`
-   **Access Swagger REST API UI to browse and test the REST API**: `login:karaf Pass:karaf`

## How to Verify Unomi is Working

You can check Unomi's health status by running this `curl` command in your terminal:

```bash
curl http://localhost:8181/cxs/health
