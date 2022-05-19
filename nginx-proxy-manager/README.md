# Nginx Proxy Manager

- Create folder

    ```sh
    mkdir -p /opt/nginx-proxy/{db,data,letencrypt}
    ```

- Clone repository to the server

- Copy file `docker-compose` to above folder

    ```sh
    cp -rp nginx-proxy-manager/docker-compose.yml /opt/nginx-proxy/
    ```

- Run service

    ```sh
    docker-compose up -d
    ```