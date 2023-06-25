# Setting up a Nginx docker container on remote server with Ansible

## Project Structure

```
├── docker
│   ├── docker-compose.yml
│   └── nginx
│       └── Dockerfile
└── provisioning
    ├── host_vars
    │   └── remote
    ├── hosts.yml
    ├── roles
    │   ├── app
    │   │   └── tasks
    │   │       └── main.yml
    │   └── setup
    │       ├── handlers
    │       │   └── main.yml
    │       └── tasks
    │           ├── docker.yml
    │           └── main.yml
    └── site.yml
```

## Build

```
ansible-playbook provisioning/site.yml -i provisioning/hosts.yml
```