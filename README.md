# dhis2-docker

Local DHIS2 instance via Docker Compose.

## Requirements

- Windows 10/11 64-bit with WSL 2, or Linux/macOS
- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- At least 4 GB of RAM available
- Port 8080 free

## Project structure

```
dhis2-docker/
├── docker-compose.yml
└── dhis2-home/
    └── dhis.conf
```

## Usage

### Start

```bash
docker compose up -d
```

### Check status

```bash
docker compose ps
```

### Follow logs

```bash
docker compose logs -f web
```

DHIS2 is ready when the logs show `Server startup in XXXX ms`.

### Access

Open [http://localhost:8080](http://localhost:8080) in your browser.

Default credentials:

| Field    | Value    |
|----------|----------|
| Username | admin    |
| Password | district |

Change the default password after first login.

### Stop

```bash
docker compose down
```

### Full reset (deletes all data)

```bash
docker compose down -v
```

## Notes

- First startup may take 2 to 5 minutes.
- Docker will automatically pull all required images on first run.
- The default installation starts with an empty database.

## License

MIT