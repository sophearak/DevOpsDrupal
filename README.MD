##Up and Running Drupal with Lazy Mood!!!

This setup have out of the box:
- Nginx
- MySql
- PHP5
- Drush
- Drupal


## How to use?

1. Make you have Vagrant and Ansible install
2. Clone the repo `git clone https://github.com/sophearak/DevOpsDrupal.git`
3. Change directory `cd DevOpsDrupal`
4. create www folder `mkdir www`
5. make sure host file information is correct `./ansible/host`
6. `cd ansible && ansible-playbook -i host playbook.yml`

Note:
- you can check your ssh-key by `vagrant ssh-config`
- you can check your ip by login to your server by `vagrant ssh` then run `ifconfig` or `/sbin/ifconfig`


