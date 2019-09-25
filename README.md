# Ansible role 'ansible-role-syslogserver'

An Ansible role for setting up rsyslog on a central syslog server.

## Requirements
This role should work for Debian- and RedHat-family distributions. Testing has only been done on CentOS7 though, but feel free to provide feedback regarding issues with your particular distribution (both if it works and if it doesn't) and I will try to update the role accordingly.

## Role Variables
| Variable		| Default		| Comments (type) |
| :---			| :---			| :---		  |
| `syslogserverPackage` | rsyslog | rsyslog package name |
| `syslogserverService` | rsyslog | rsyslog service name |
| `syslogserverListenPort` | 514 | Port (TCP or UDP) rsyslog should listen to |
| `syslogserverRemoteLogsBasePath` | `/var/log` | Base path where remote logs will be stored |
| `syslogserverUDP` | `false` | Wether to listen for syslog messages over UDP. When set to `false`, TCP will be used, if set to `true` UDP will be used. |
## Dependencies

## Example Playbook
```Yaml
- hosts: syslogservers
  become: true
  roles:
    - role: ansible-role-syslogserver
```

## Testing


## License

BSD

## Contributors

Issues, feature requests, ideas, suggestions, etc. are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Please create a topic branch for your proposed changes, it's the easiest way to merge back into the project.

- [Oscar Petersson](https://github.com/oscpe262/) (Maintainer)
