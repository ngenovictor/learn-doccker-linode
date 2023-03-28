# Docker Playing

A simple project to experiment with deploying a django app with docker on linode.

The goal is to have minimal installations on the linode server and be able to quickly deploy apps on an instance.

The aim is to also have all my experiment apps live on docker and all be deployed to one running server since the downfall of heroku free tier.

I also want to be able to reuse existing images to deploy different parts of apps I will be using.

## Instructions

- Create a linode server
- Install docker on the server. Follow the instructions in https://docs.docker.com/engine/install/ubuntu/
- Copy the project files to the linode server using `rsync`
    ```shell
    rsync -avv -e ssh --exclude="*.pyc" --exclude="**/env" . root@178.79.163.94:/root/django-docker
    ```
- SSH back into the server and run `docker compose up -d` in the directory with the docker compose file, where `-d` is so that the app can run in the background.
