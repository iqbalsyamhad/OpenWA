docker compose -f docker-compose.custom.dev.yml -p newopenwa --profile full up -d

** Create CRM user & database **
CREATE USER crm_user WITH PASSWORD 'change-me-crm-db-password';
CREATE DATABASE crm_db OWNER crm_user;
GRANT ALL PRIVILEGES ON DATABASE crm_db TO crm_user;

