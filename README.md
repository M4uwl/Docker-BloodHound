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

---

## Deployment Steps

### Step 1: Clone the Repository

First, download or clone the repository from GitHub:

```bash
git clone https://github.com/M4uwl/Docker-BloodHound
```

Then enter the project directory:

```bash
cd Docker-BloodHound
```

---

### Step 2: Rename the Environment File

Rename the `env` file to `.env` before using the Docker Compose deployment.

From **PowerShell**, you can run:

```powershell
Rename-Item env .env
```

---

### Step 3: Install Docker Desktop

To run this project on a Windows system, you need to install **Docker Desktop**.

Download it from:

```text
https://www.docker.com/products/docker-desktop/
```

Once installed, make sure Docker Desktop is running before continuing.

---

### Step 4: Open PowerShell in the Project Directory

Navigate to the directory where the repository is located.

For example:

```powershell
cd .\Docker-BloodHound\
```

All Docker commands must be executed from the folder where the `docker-compose.yml` and `.env` files are located.

---

### Step 5: Start the BloodHound Docker Environment

Run the following command from PowerShell:

```powershell
docker compose --env-file .\.env -p Project_Name up -d
```

Replace:

```text
Project_Name
```

with the name you want to assign to the Docker project.

For example:

```powershell
docker compose --env-file .\.env -p bloodhound-lab01 up -d
```

This command will start the Docker environment using the variables defined in the `.env` file.


