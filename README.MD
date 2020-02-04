
##### Запуск сервисов

* `docker-compose pull`
* `docker-compose up -d`

##### Это запускает следующие сервисы:

| NAME     | DESCRIPTION                                                    | PORT(S) | ENVIRONMENT(S)                                     |
| :------- | :--------------------------------------------------------------| ------- | -------------------------------------------------- |
| php      | The API with PHP, PHP-FPM 7.3, Composer and sensitive configs  | n/a     | all                                                |
| db       | A PostgreSQL database server                                   | 5432    | all (prefer using a managed service in prod)       |
| client   | A development server for the Progressive Web App               | 443     | dev (use a static website hosting service in prod) |
| admin    | A development server for the admin                             | 444     | dev (use a static website hosting service in prod) |
| api      | The HTTP server for the API (NGINX)                            | n/a     | all                                                |
| vulcain  | The Vulcain gateway                                            | 8443    | all                                                |
| mercure  | The Mercure hub, for real-time capabilities                    | 1337    | all (prefer using the managed version in prod)     |

##### Чтобы увидеть журналы контейнера, запустите:
* `docker-compose logs -f`
