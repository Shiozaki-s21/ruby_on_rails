#起動時command
##立ち上げ
>$ docker-compose run --rm web rails new . --force --database=mysql --skip-bundle
>$ docker-compose build

##DB作成
>$ docker-compose up
>$ <ctrl-C>
>$ docker-compose run --rm web rake db:create


