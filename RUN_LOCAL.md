docker compose -f docker-compose.custom.dev.yml -p newopenwa --profile full up -d

prod:
sudo docker compose -f docker-compose.custom.yml --env-file .env.production --profile full up -d --build


** Create CRM user & database **
CREATE USER crm_user WITH PASSWORD 'change-me-crm-db-password';
CREATE DATABASE crm_db OWNER crm_user;
GRANT ALL PRIVILEGES ON DATABASE crm_db TO crm_user;
