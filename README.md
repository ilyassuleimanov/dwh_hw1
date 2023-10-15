# dwh_hw1

Поднимается инстанс postgresql + репликация, скрипт для инициализации по требуемой в задании схеме - это "initdb.sql". Контейнер мастера назван "docker_repl_v2-postgresql-master-1", слейва - "docker_repl_v2-postgresql-slave-1". После запуска можно проверить, что в слейве появились все таблицы.

Запуск:

- docker compose up
- docker exec -it docker_repl_v2-postgresql-master-1 sh -c "PGPASSWORD=my_password psql -h localhost -U my_user -d my_database < /docker-entrypoint-initdb.d/initdb.sql"
