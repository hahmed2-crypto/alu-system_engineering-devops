# Web Server

This project covers setting up, configuring, and automating an **Nginx** web server on an Ubuntu machine, configuring DNS records for a custom `.tech` domain, handling HTTP redirections, and serving custom error pages.

## Learning Objectives
* What the main role of a web server is
* What a child process is and why web servers usually have a parent process and child processes
* What the main HTTP requests are (`GET`, `POST`, `PUT`, `DELETE`, `HEAD`)
* What DNS stands for and what its main role is
* What DNS record types are (`A`, `CNAME`, `TXT`, `MX`)

## Requirements
* All scripts are interpreted on **Ubuntu 20.04 LTS**
* All Bash scripts are executable (`chmod +x`) and pass `shellcheck` without errors
* The first line of all Bash scripts is `#!/usr/bin/env bash`
* `systemctl` is not used to restart Nginx (`service nginx restart` is used instead)

## Project Files

| File | Description |
| :--- | :--- |
| `0-transfer_file` | Bash script that transfers a file from a client to a server using `scp` with strict host key checking disabled. |
| `1-install_nginx_web_server` | Bash script that installs Nginx, configures it to listen on port `80`, and serves a root page containing `Holberton School`. |
| `2-setup_a_domain_name` | Contains the registered `.tech` root domain name (`cracycamel.tech`) configured with an `A` record pointing to the server IP. |
| `3-redirection` | Bash script that installs Nginx and configures `/redirect_me` to return a `301 Moved Permanently` redirect. |
| `4-not_found_page_404` | Bash script that installs Nginx, configures the `301` redirect, and serves a custom `404` error page containing `Ceci n'est pas une page`. |
| `5-design_a_beautiful_404_page.html` | Custom HTML/CSS 404 error page designed with space-themed styling while retaining the required `Ceci n'est pas une page` message. |

## Usage

### Transfer a File (`0-transfer_file`)
```bash
./0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY
```

### Configure the Web Server
Run any of the configuration scripts as `root` on a fresh Ubuntu server:
```bash
sudo ./1-install_nginx_web_server
sudo ./3-redirection
sudo ./4-not_found_page_404
```

## Author
* **hahmed2-crypto** — ALU System Engineering & DevOps

