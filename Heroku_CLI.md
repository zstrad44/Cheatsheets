Some useful commands.

### Clone existing heroku app

    heroku git:clone -a [existing app name]
### Deploy staging

    git push staging master

### Add new instance for git deploy

    git remote add staging git@heroku.com:appname.git

### Capture and Download database postgress/ ruby
#### Capture the DB

	heroku pg:backups:capture
	###Download the DB
	heroku pg:backups:download
#### Then to load the DB as the local db

	pg_restore --verbose --clean --no-acl --no-owner -h localhost -U [Enter PG Username] -d [Enter PG DB name] latest.dump
