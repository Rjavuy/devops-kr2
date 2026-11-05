# KR2 template

Counter service on Flask + Redis.

Local run: `pip install -r requirements.txt && flask --app app run`

## Deployment (KR2, variant 4)

- Server: `devops-vm`, project in `~/kr2`, secret `~/kr2/.env` (mode 600, see `.env.example`).
- Run: `docker compose up -d --build` — app `kr2-app:1.0` on `127.0.0.1:8004`, Redis 7 (Alpine) with password and volume `redis_data`.
- Published by Nginx: `https://kv.devops.local` (`deploy/nginx/kr2` → `/etc/nginx/sites-available/kr2`, certificate `/etc/ssl/certs/kr2.crt`).
