# Docker-BloodHound

**Docker-BloodHound** is a repository that includes the two required files to deploy multiple BloodHound instances without risking the corruption of information from a single shared instance.

It allows you to easily customize key variables such as:

- Instance names
- Database names
- Access passwords
- Exposed ports

This makes it simple to run and manage different BloodHound environments independently, keeping each deployment isolated and avoiding conflicts between datasets.


## How It Works

This repository includes two configuration files:

- `docker-compose.yml`
- `env`

The `docker-compose.yml` file should not be modified unless you want to make specific changes to the deployment configuration.

The `env` file contains the environment variables required by the Docker deployment. In this repository, it is uploaded without the hidden file prefix so it can be stored properly in GitHub.

Before using it, you must rename:

```bash
env
```

to:

```bash
.env
```

## Requirements

To run this project on a Windows system, you need to install **Docker Desktop**.

## Deployment Commands

Once Docker Desktop is installed and running, use the following commands from the folder where the project files are located:

```bash
docker compose --env-file .\.env -p Project_Name up -d
```

Replace:

```bash
Project_Name
```

with the name you want to assign to the Docker project.
