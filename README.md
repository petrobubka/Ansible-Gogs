# Ansible Gogs

This repository contains Ansible playbooks and roles for deploying and managing Gogs, a self-hosted Git service, on remote servers. It automates the installation and configuration process, allowing you to quickly set up a Gogs instance with minimal manual intervention. It uses 1 nfs sever, 1 db server, 1 load balancer server and desired amount of workers(apps).

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)

## Introduction

Gogs is a lightweight, open-source Git service written in Go. It provides a self-hosted platform for managing and collaborating on Git repositories. With the help of Ansible, this project aims to simplify the deployment and management of Gogs instances across multiple servers.

## Features

- Automated installation and configuration of Gogs on remote servers.
- Support for customizing various Gogs settings, such as database configuration and repository storage.
- Seamless management of multiple Gogs instances on different servers.
- Ability to easily scale the Gogs infrastructure as per your requirements.
- Simplified maintenance and updates of Gogs instances using Ansible playbooks.

## Requirements

To use this Ansible project, you need:

- Ansible installed on your local machine.
- Target servers running a compatible operating system (e.g., Ubuntu, CentOS) with SSH access.
- Basic understanding of Ansible and Git concepts.

## Usage

To deploy Gogs on your target servers, follow these steps:

1. Clone this repository to your local machine: `git clone https://github.com/petrobubka/ansible_gogs.git`
2. Navigate to the repository directory: `cd ansible_gogs`
3. Edit the `hosts` file and specify the target servers where you want to deploy Gogs.
4. Change file with database credentinals in `inventory/group_vars/dbvars.yml`  . Default vault passworrd is `pass`
5. Run the Ansible playbook: `ansible-playbook -i inventory/production/hosts site.yml --ask-vault-pass`

Once the playbook execution completes, Gogs should be successfully installed and configured on the target servers.

## Configuration

The project provides a set of configuration options to customize your Gogs deployment. The main configuration file is in `hosts`, which includes ip_addresses for your machines, there you can choose how many workers(apps) will be used for load balancing.


## Contributing

Contributions to this project are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request. Make sure to follow the contribution guidelines outlined in the repository.
