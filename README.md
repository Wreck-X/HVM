# HVM

## Installing Docker

1) Set up Docker's apt repository.
```# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

2) To install the latest version
``` 
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3) Verify that the Docker Engine installation is successful by running the hello-world image.

```
sudo docker run hello-world
```

## Deploying Frontend and backend

```
git clone https://github.com/Wreck-X/HVM && cd HVM && docker compose up --build
```

* Frontend will be deployed at **localhost:3000**
* Backend will be deployed at **localhost:8000**

## Credentials
`docker-compose.yml` contains variables for `DJANGO_SUPERUSER_USERNAME`,`DJANGO_SUPERUSER_PASSWORD` and `DJANGO_SUPERUSER_EMAIL=admin@example.com`, Which allow for modification for login credentials

**By default Username - admin, Password - admin.**