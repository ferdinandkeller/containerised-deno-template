# Containerised Deno Template

This repo contains the template needed to startup a containerised Deno project. This is really useful to develop multiple projects locally in parallel without having their dependencies clash against each-others (language or package version for example). It also allows us to be free of the "works on my machine" and "took hours to install the correct dependencies" problems.

Here are the features available:
- The host's SSH auth socket is mounted inside the container
- The host's `~/.ssh` directory is available as read-only
- The host's `~/.gitconfig` file is available as read-only
- There is a nice looking bash prompt
- The user isn't root but can use sudo without a password

You can start this project in a **Docker Development Environment** by [clicking this link](https://open.docker.com/dashboard/dev-envs?url=git@github.com:ferdinandkeller/containerised-deno-template.git).