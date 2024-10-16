# pulp-regen-cert

Playbook to regenerate a Pulp server web certificate, based on Pulp Ansible roles


Requisites:

- python-cryptography for your discovered python version (in my case, python39-cryptography)
- community.crypto ansible collection (probably already installed in most cases)


**Backup your pulp directory, in my case this was `/etc/pulp/`**

**Edit the playbook to change the variables, including your server's hostname.**


How to run:

```
ansible-playbook -i hosts --limit localhost pulp-regen-cert.yaml
nginx -t && service nginx restart
```



