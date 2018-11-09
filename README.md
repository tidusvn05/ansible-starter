# ansible-starter
Ansible playbook for beginner

## Sample playbooks
1. setup webserver
2. Use loop to setup git for many sites

## Usages:
- Check any playbook file.
- Edit inventory file, eg: testing_hosts, change to your server IP. 
- Check variables file in vars that playbook be using.
- Edit playbook for your purpose.
- Run playbook:
  ansible-playbook -i <inventory_file> playbook.yml
  => With sample 1: ansible-playbook -i testing_hosts playbook_setup_webserver.yml

## Directory Structure:
.
├── README.md
├── playbook_setup_webserver.yml
├── playbook_use_loop.yml
├── production_hosts
├── roles
│   ├── config_dkim_for_new_domain
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   │       └── nginx-http.j2
│   ├── config_nginx_sendy_vhost
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   │       └── nginx-le-sendy.j2
│   ├── config_nginx_static_vhost
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   │       └── nginx-le-static.j2
│   ├── setup_all_sites
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   ├── setup_git_project
│   │   └── tasks
│   │       └── main.yml
│   ├── setup_letsencrypt
│   │   └── tasks
│   │       └── main.yml
│   ├── verify_letsencrypt
│   │   ├── tasks
│   │   │   └── main.yml
│   │   └── templates
│   │       └── nginx-http.j2
│   └── verify_letsencrypt_apache
│       ├── tasks
│       │   └── main.yml
│       └── templates
│           └── apache-http.j2
├── templates
├── testing_hosts
└── vars
    ├── common.yml
    ├── loop_data.yml
    └── webserver.yml

## Author
Tidusvn05 <tidusvn05@gmail.com>

## Licence 
MIT

