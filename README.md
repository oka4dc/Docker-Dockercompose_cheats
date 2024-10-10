# Django-Docker-Dockercompose_cheats
# compiled by: Dennis Okafor
## okaforchikelue93@gmail.com

# Basic Commands

### django-admin startproject <project_name>
# Creates a new Django project with the specified project name.

python manage.py runserver
# Starts the development server to run the Django application.

python manage.py startapp <app_name>
# Creates a new Django application with the specified app name inside the project.

python manage.py makemigrations
# Detects changes in models and creates migration files.

python manage.py migrate
# Applies the migrations to the database.

python manage.py createsuperuser
# Creates a superuser with admin access.

python manage.py shell
# Opens an interactive Python shell with Django settings and models loaded.

python manage.py check
# Checks for any issues in the project without running migrations.

python manage.py showmigrations
# Displays a list of all migrations and their status.

python manage.py sqlmigrate <app_name> <migration_number>
# Shows the raw SQL of a specific migration.

python manage.py collectstatic
# Collects static files from all apps into a single directory.

python manage.py test
# Runs all tests in the project.

# Intermediate Commands

python manage.py flush
# Deletes all data in the database but keeps the schema (useful for resetting the database).

python manage.py dbshell
# Opens the database shell (works for supported databases like PostgreSQL, MySQL, etc.).

python manage.py loaddata <fixture_name>
# Loads data from the specified fixture into the database.

python manage.py dumpdata <app_name>.<model_name>
# Dumps the data of a model into JSON, XML, or YAML format.

python manage.py diffsettings
# Displays differences between the current settings and Django's default settings.

python manage.py sqlflush
# Returns the SQL statements required to delete all data from the database (doesn't apply them).

python manage.py clearsessions
# Deletes expired sessions from the database.

python manage.py inspectdb
# Generates Django models from an existing database schema.

python manage.py sendtestemail
# Sends a test email to the email addresses specified in the command.

# Advanced Commands

python manage.py dbshell
# Opens a database shell for direct interaction with your database.

python manage.py changepassword <username>
# Changes the password for the specified user.

python manage.py showmigrations --plan
# Shows the migration plan, indicating which migrations are applied and which are not.

python manage.py migrate --fake <app_name> <migration_number>
# Marks a migration as applied without actually running it (useful for resolving migration conflicts).

python manage.py migrate --run-syncdb
# Forces Django to create database tables for apps without migrations (used with caution).

python manage.py testserver <fixture_file>
# Runs a development server with data loaded from a fixture.

python manage.py makemessages -l <language_code>
# Extracts translatable strings for the specified language.

python manage.py compilemessages
# Compiles the message files created by `makemessages` for translations.

python manage.py startproject --template=<template_url> <project_name>
# Creates a new Django project from a custom project template.

python manage.py check --deploy
# Performs checks for deployment best practices.

python manage.py runserver_plus
# Starts the development server with advanced debugging features (requires `django-extensions`).

python manage.py graph_models <app_name>
# Generates a graphical representation of the model dependencies (requires `django-extensions`).

# Docker Commands

# Pull an image from a Docker registry (default: Docker Hub)
docker pull <image_name> 

# Run a container from an image
docker run <image_name>

# Run a container in the background (detached mode)
docker run -d <image_name>

# Run a container with an interactive shell
docker run -it <image_name> /bin/bash

# List all running containers
docker ps

# List all containers (including stopped ones)
docker ps -a

# Stop a running container
docker stop <container_id>

# Start a stopped container
docker start <container_id>

# Restart a running container
docker restart <container_id>

# Remove a stopped container
docker rm <container_id>

# Remove a Docker image
docker rmi <image_name>

# Build a Docker image from a Dockerfile
docker build -t <image_name> .

# View logs of a running container
docker logs <container_id>

# Follow logs of a container in real-time
docker logs -f <container_id>

# Execute a command in a running container
docker exec -it <container_id> <command>

# View system-wide Docker information
docker info

# List all Docker images
docker images

# Remove dangling images
docker image prune

# Remove all stopped containers and dangling images
docker system prune

# View disk usage by Docker
docker system df

# Push an image to Docker Hub (after logging in)
docker push <username>/<image_name>

# Login to Docker Hub
docker login

# Tag an image for pushing to a registry
docker tag <local_image_name> <username>/<image_name>:<tag>

# Save an image to a tar file
docker save -o <output_file>.tar <image_name>

# Load an image from a tar file
docker load -i <image_file>.tar

# Inspect the details of a container
docker inspect <container_id>

# Attach to a running container’s terminal
docker attach <container_id>

# Show resource usage of containers
docker stats

# Show changes made in a container’s filesystem
docker diff <container_id>


# Docker Compose Commands

# Create and start containers based on the docker-compose.yml file
docker-compose up

# Start containers in the background (detached mode)
docker-compose up -d

# Stop and remove containers, networks, and volumes
docker-compose down

# Stop containers without removing them
docker-compose stop

# Restart containers
docker-compose restart

# View logs from all containers in real-time
docker-compose logs

# Follow logs of specific service in real-time
docker-compose logs -f <service_name>

# Build or rebuild services
docker-compose build

# List all running containers from docker-compose
docker-compose ps

# Execute a command in a running container from docker-compose
docker-compose exec <service_name> <command>

# View the configuration of docker-compose.yml
docker-compose config

# Scale the number of containers for a service
docker-compose scale <service_name>=<count>

# Stop and remove all containers, networks, and volumes created by `up`
docker-compose down -v

# Run a one-time command against a service
docker-compose run <service_name> <command>

# Remove stopped service containers
docker-compose rm
