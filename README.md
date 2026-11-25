# FileBrowser

A web file manager for the qBittorrent downloads folder.

## Setup
1. `cp .env.example .env`, then set `DOWNLOADS_PATH` (same as qBittorrent's) and `PUID`/`PGID` (`id -u` / `id -g`).
2. `mkdir -p config database` so the folders are owned by you, not root.
3. `docker compose up -d`
4. Get the initial admin password: `docker logs filebrowser`
5. Log in at `http://localhost:8081` and change the password.

Only the downloads folder is mounted (at `/srv/downloads`). To upgrade, change `FB_VERSION` in `.env` and run `docker compose up -d`.
