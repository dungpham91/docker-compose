# Deploy stack monitoring Prometheus-Grafana with Docker Compose

- Edit information that you need on the file [grafana.ini](./grafana/grafana.ini), for example change the default admin account is `admin:admin`.

```ini
#################################### Security ############################
[security]
# disable creation of admin user on first start of grafana
disable_initial_admin_creation = false

# default admin user, created on startup
admin_user = admin

# default admin password, can be changed before first start of grafana, or in profile settings
admin_password = admin
```

- Update configurations for Prometheus with your all exporters. Open and edit the file [prometheus.yml](./prometheus/prometheus.yml).

- You can specify image version for Prometheus, Grafana and Node Exporter by edit the file [docker-compose.yml](./docker-compose.yml). Select the line `image:` and change your needed version, for example:

```yml
image: prom/prometheus:v2.35.0
```

- Run up the compose

```sh
docker-compose up -d

# Or use newest version Docker Compose command
docker compose up -d
```

- Stop and delete compose

```sh
docker-compose down

# Or use newest version Docker Compose command
docker compose down
```

- After run up the compose, access Prometheus with this link [http://localhost:9090](http://localhost:9090).

- Access Grafana with link [http://localhost:3000](http://localhost:3000) and default admin account to login is: `admin / admin`.