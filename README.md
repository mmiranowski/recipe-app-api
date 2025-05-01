# recipe-app-api
docker compose run --rm app sh -c "python manage.py startapp <app-name>"



# run tests
docker compose run --rm app sh -c "python manage.py test"

# run wait for db command
docker compose run --rm app sh -c "python manage.py wait_for_db"

# run command + linting
docker compose run --rm app sh -c "python manage.py wait_for_db && flake8"


## Python Migrations

# Make migrations
Automatically generetes migration file based on your model class or apply changes to existing migration files.

docker compose run --rm app sh -c "python manage.py makemigrations"

# Apply migrations
When you are ready to migrate your database to a different type of database

python manage.py migrate

Run it after waiting for database


# Admin user
email: admin@example.com
pass: test123