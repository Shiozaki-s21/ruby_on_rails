#起動時command
##立ち上げ
>$ docker-compose run --rm web rails new . --force --database=mysql --skip-bundle
>$ docker-compose build
---

##DB作成
>$ docker-compose up
>$ <ctrl-C>
>$ docker-compose run --rm web rake db:create
---

#scaffoldの実行
> rails generate scaffold User name:string email:string
> docker-compose run --rm web rails g scaffold item name:string amount:integer memo:text
> docker-compose run web rails g scaffold User name:string email:string
> docker-compose run --rm web rake db:migrate
---

#
docker-compose run --rm web rails g scaffold User name:string email:string
docker-compose run --rm web rake db:migrate
db:migrate RAILS_ENV=development

docker-compose run --rm web rails g scaffold item name:string amount:integer memo:text
docker-compose run --rm web rails g scaffold User name:string email:string
                            rails g scaffold user name:string age:integer
docker-compose run --rm web rake db:migrate
---
#Dockerでrailsコマンド実行
> docker-compose run app rails [rails_command]