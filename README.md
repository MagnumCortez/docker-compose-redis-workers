# docker-compose-redis-workers
Gerenciamento de containers (Frontend, Python, Postgres, Redis e Workers)
Simples projeto para simular um ambiente de produção.

### Comandos Basicos

* Subir todos serviços
```sh
docker-composer up -d
```

* Subir todos serviços com 3 instancias do serviço worker
```sh
docker-composer up -d --scale worker=3
```

* Parar todos serviços
```sh
docker-composer down
```

* Log dos serviços
```sh
docker-compose logs -f -t
```

* Log apenas dos serviços worker
```sh
docker-compose logs -f -t worker
```

* Executando um comando no serviço db
```sh
docker-compose exec db psql -U postgres -d email_sender -c 'select * from emails'
```
