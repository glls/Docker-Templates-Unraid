# Docker Templates for Unraid

glls repository for [Unraid](https://unraid.net/) Docker templates

## Available Templates

Below is a list of the Docker templates currently available, along with links to their official project sites for more information.

---

### 1. TimescaleDB

- **Description:** TimescaleDB is an open-source time-series SQL database engineered for speed, scale, and reliability. It's packaged as a PostgreSQL extension and is ideal for a wide range of applications, including IoT, monitoring, analytics, and financial data.
- **Official Website:** [timescale.com](https://www.timescale.com/)
- **GitHub Repository:** [github.com/timescale/timescaledb](https://github.com/timescale/timescaledb)
- **Docker Image:** [hub.docker.com/r/timescale/timescaledb](https://hub.docker.com/r/timescale/timescaledb)

---

### 2. TimescaleDB-HA (High Availability)

- **Description:** This template provides a High Availability setup for TimescaleDB, typically utilizing Patroni for automated failover and PostgreSQL's streaming replication. This ensures greater uptime and data redundancy for your time-series data.
- **Official Documentation (High Availability):** [docs.timescale.com/self-hosted/latest/replication-and-ha/about-ha/](https://docs.timescale.com/self-hosted/latest/replication-and-ha/about-ha/)
- **Docker Image (includes Patroni):** [hub.docker.com/r/timescale/timescaledb-ha](https://hub.docker.com/r/timescale/timescaledb-ha)
- **GitHub Repository (for Docker HA setup):** [github.com/timescale/timescaledb-docker-ha](https://github.com/timescale/timescaledb-docker-ha)

---

### 4. go-vod (not using it anymore)

- **Description:** go-vod is a Extremely minimal on-demand video transcoding server in go.
- **Documentation:** [https://memories.gallery/hw-transcoding/#overview](https://memories.gallery/hw-transcoding/#overview)
- **GitHub Repository:** [https://github.com/pulsejet/memories/tree/master/go-vod](https://github.com/pulsejet/memories/tree/master/go-vod)

---

## Notes

### Listing Available Extensions in TimescaleDB/PostgreSQL

If you need to see all the extensions that are available to be installed (or are already installed) in your TimescaleDB or standard PostgreSQL instance, you can run the following SQL query. This is useful for checking if a specific extension (like `timescaledb` itself, or others such as PostGIS, etc.) is present and ready for use.

**How to run the query:**

1. Connect to your PostgreSQL/TimescaleDB database using a SQL client (e.g., `psql`, DBeaver, pgAdmin).
2. Execute the following command:

```sql
SELECT name, default_version, installed_version, comment
FROM pg_available_extensions;
```
