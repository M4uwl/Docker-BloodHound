# Docker-BloodHound

**Docker-BloodHound** is a repository that includes the two required files to deploy multiple BloodHound instances without risking the corruption of information from a single shared instance.

It allows you to easily customize key variables such as:

- Instance names
- Database names
- Access passwords
- Exposed ports

This makes it simple to run and manage different BloodHound environments independently, keeping each deployment isolated and avoiding conflicts between datasets.


## How It Works

The repository includes two configuration files:

- `docker-compose.yml`
- `env`

The `docker-compose.yml` file should not be modified unless you want to make specific changes to the deployment configuration.

The `env` file contains the environment variables required to customize the deployment. In this repository, it is uploaded without the hidden-file format so it can be safely included in GitHub.

Before using it, rename the file from:

```text
env
```
To:
```text
.env
```
