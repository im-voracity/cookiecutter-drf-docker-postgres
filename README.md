# Getting started

## Project Settings

The default configuration for this project is as follows:

- Dockerized Django Application
- PostgreSQL Database
- Custom app "core" with a custom Django User model (email instead of username, First Name, Last Name as optional fields)
- Custom `management.py` command `wait_for_db` to wait for the database to be available, it launches automatically on 
docker-compose up.
- By default, migrations are applied with every run of the container, but it can be disabled in `docker-compose.yml` file
- Flake8 is also installed by default when dev variable it's set to true in the `docker-compose.yml` file.
- Github actions are automatically available and runs tests for every push to the repository.

## Recommended Changes

You should change the versions inside the `requirements.txt` and `requirements.dev.txt` file to the versions you 
want to use in your project.

## Docs folder
1. `README.md` well, everyone knows how this file works right? Change it to your project's needs.
2. `README.dev.md` this file was built thinking of open source projects, with something that will help contributors.
3. `ISSUES.md` this file is for writing down issues, I myself usually find myself getting stuck on a problem withing a 
project and found very useful to use this file to write down the problem and the solution, so I can come back to it later.
Usually when finishing up my projects, I write them down in a more structured way inside the `README.dev.md` and delete
this file.
4. Make sure you go to the `.github/workflows` folder and change the `checks.yml` file to your project's needs.
