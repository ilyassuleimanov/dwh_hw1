# dwh_hw1

Поднимается инстанс postgresql + репликация, скрипт для инициализации по требуемой в задании схеме - это "initdb.sql". Контейнер мастера назван "dwh_hw1-main-postgresql-master-1", слейва - "dwh_hw1-main-postgresql-slave-1". После запуска можно проверить, что в слейве появились все таблицы.

Запуск:

- docker compose up
- docker exec -it dwh_hw1-main-postgresql-master-1 sh -c "PGPASSWORD=my_password psql -h localhost -U my_user -d my_database < /docker-entrypoint-initdb.d/initdb.sql"
