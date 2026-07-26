# WebUI Local Run Notes

## Pass .env.local.example to Docker Compose

Use the following command to pass variables from `.env.local.example` to `docker compose`.

```bash
docker compose --env-file .env.local.example up -d
```

This resolves `${LANGFUSE_PUBLIC_KEY}` and `${LANGFUSE_SECRET_KEY}` in `docker-compose.yml`.

## Verify substitution

```bash
docker compose --env-file .env.local.example config
docker compose exec litellm env | grep LANGFUSE
```
