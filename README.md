# sqlalchemy-practice
SQLAlchemy ORM Tutorial: This repository contains an implementation of a simple database schema for a movie library, created using SQLAlchemy ORM and PostgreSQL

I followed a SQLAlchemy tutorial where i learned how to map Python classes to database tables using SQLAlchemy's declarative system. Then inserted some data into these tables and performed queries on them.

The tutorial also covered how to use SQLAlchemy ORM to query data, making it easy to retrieve and manipulate data. 

Lastly, we dockerized our PostgreSQL database instance for easy setup and teardown.

## How to Run?

### Step 1: Install Docker
First, you need to have Docker installed on your system. You can download Docker [here](https://www.docker.com/products/docker-desktop).

### Step 2: Create Dockerized PostgreSQL Instance
After having Docker installed, you can create a dockerized PostgreSQL instance with the following command:

docker run --name sqlalchemy-orm-psql \
    -e POSTGRES_PASSWORD=pass \
    -e POSTGRES_USER=usr \
    -e POSTGRES_DB=sqlalchemy \
    -p 5432:5432 \
    -d postgres

## Step 3: Install Python Dependencies
Next, we need to install the necessary Python dependencies:
pipenv install sqlalchemy psycopg2-binary

## Step 4: Run the Python Script
Finally, we can run our Python script:
pipenv shell
python inserts.py

To destroy the dockerized PostgreSQL instance, you can use the following command:
docker rm -f sqlalchemy-orm-psql

## Requirements
Docker
Python 3
pipenv
