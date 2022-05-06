Connect string
User ID=doska;Password=secret;Host=doska.kupeyka.com;Port=5432;Database=doska;Pooling=true;Min Pool Size=0;Max Pool Size=100;Connection Lifetime=0;

Export to dump
docker exec -u <your_postgres_user> <postgres_container_name> pg_dump -Fc <database_name_here> > db.dump

Export from dump
docker exec -i -u <your_postgres_user> <postgres_container_name> pg_restore -C -d postgres < db.dump