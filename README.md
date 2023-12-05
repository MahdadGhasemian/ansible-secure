# Ansible Role: Secure

Essential Security For First 5 Minutes On A Server

## Requirements

None.

## Role Variables
```yaml
# /home/server_user
server_user: newuser
home_path: "/home/{{ server_user }}"

# SSH
ssh_port: 2220
user_authorized_key_path: "files//id_rsa.pub"

# Firewall
external_ports:
  - 22
  - 80
  - 443
external_range_ports:
  - range: "10000:10001"
    proto: "tcp"
```

## Dependencies

None.

## Example Playbook (using default package)

    - hosts: servers
      roles:
        - role: MahdadGhasemian.ansible-secure

## License

MIT / BSD

## Author Information

This role was created in 2023 by [Mahdad Ghasemian](https://mahdad.me/).