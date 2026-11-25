# homelab-services

Small self-hosted services, one folder (and one Compose project) each.

| Service | What | Port |
|---|---|---|
| `gitea/` | Git hosting | 3000 (web), 2222 (ssh) |
| `minio/` | S3-compatible object storage | 9000 |
| `kiwix/` | Offline Wikipedia & other ZIM archives | 8083 |
| `invoiceplane/` | Invoicing | 8084 |
| `portainer-agent/` | Agent for a remote Portainer | 9001 |

Each service keeps its state in its own `data/` (and `db/`) folder, which is git-ignored.
Secrets go in a per-service `.env` (see each `.env.example`).

```bash
cd minio && cp .env.example .env && docker compose up -d
```
