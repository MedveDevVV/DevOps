# DevOps

Проект для запуска микросервисов frontend и backend с помощью Docker Compose. Используются версии `v2.1`.

## Запуск на Windows

1. Установить и запустить Docker Desktop.
2. Открыть PowerShell в папке с файлом `docker-compose.yml`.
3. Отключить BuildKit и запустить сборку:

```powershell
$env:DOCKER_BUILDKIT=0
docker compose build
docker compose up -d
```

## Запуск на Linux

1. Установить Docker Engine и Docker Compose.
2. Перейти в папку с файлом `docker-compose.yml`.
3. Выполнить команды:

```bash
docker compose build
docker compose up -d
```

## Использование

Открыть в браузере:

http://localhost:5173

Frontend взаимодействует с backend через Nginx и внутреннюю Docker-сеть. Данные сохраняются в Docker volume.

## Остановка

На Windows и Linux:

```bash
docker compose down
```
