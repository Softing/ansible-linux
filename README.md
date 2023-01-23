# Ansible Collection - softing.linux

## Available roles

### softing/linux/hostname

This role sets a permanent hostname

```yaml
- ansible.builtin.include_role:
    name: softing/linux/hostname
  vars:
    linux_hostname_hostname: "full.qualified.hostname.com"
```

### softing/linux/hosts

This role adds entries to the /etc/hosts file

```yaml
- ansible.builtin.include_role:
    name: softing/linux/hosts
  with_items: "{{ groups['swarm'] }}"
  vars:
    linux_hosts_hosts:
      - address: "127.0.0.1"
        hostnames: "hostname"
```
    
### softing/linux/locale

This role adds locales to Linux

```yaml
- ansible.builtin.include_role:
    name: softing/linux/locale
  vars:
    linux_locale_locales:
      - ru_RU.UTF-8
```

### softing/linux/software/apt

This role installs additional packages for apt to work correctly

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/apt
```

### softing/linux/software/cronic

This role installs the cronic package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/cronic
```

### softing/linux/software/curl

This role installs the curl package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/curl
```

### softing/linux/software/docker

This role installs the docker package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/docker
```

### softing/linux/software/htop

This role installs the htop package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/htop
```

### softing/linux/software/iotop

This role installs the iotop package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/iotop
```

### softing/linux/software/mailutils

This role installs the mailutils package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/mailutils
```

### softing/linux/software/mc

This role installs the mc package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/mc
```

### softing/linux/software/ping

This role installs the ping package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/ping
```

### softing/linux/software/postfix

This role installs the Postfix package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/postfix
  vars:
    linux_software_postfix_default_email: 'user@mail.com'
    linux_software_postfix_relay_user: 'user'
    linux_software_postfix_relay_password: 'password'
    linux_software_postfix_relay_server: 'smtp.mailgun.org'
    linux_software_postfix_relay_sever_port: '2525'
```

### softing/linux/software/telnet

This role installs the telnet package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/telnet
```

### softing/linux/software/unzip

This role installs the unzip package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/unzip
```

### softing/linux/software/wget

This role installs the wget package

```yaml
- ansible.builtin.include_role:
    name: softing/linux/software/wget
```

### softing/linux/timezone

This role sets the required timezone

```yaml
- ansible.builtin.include_role:
    name: softing/linux/timezone
  vars:
    linux_timezone_timezone: Europe/Berlin
```