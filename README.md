# ansible-role-lidarr

=========

Ansible Role to install lidarr, an automated downloader, watchlist, monitoring program for music.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `lidarr_user`       | lidarr | The primary user to run lidarr  |
| `lidarr_uid`        | *optional* | Commented out by default |
| `lidarr_group`      | media | The primary group for `lidarr_user` |
| `lidarr_group_gid`  | *optional* | Commented out by default |
| `lidarr_base_install_dir` | /opt | Base Install directory for lidarr |
| `lidarr_config_dir` |  /opt/data/lidarr | Data directory to store configuration |
| `lidarr_download_url` | https://lidarr.servarr.com/v1/update/master/updatefile?os=linux&runtime=netcore&arch=x64 | Link to the latest release |
| `lidarr_port` | 8686 | Port in which lidarr operates on, to add to Firewalld |
| `lidarr_packages` |   `- curl`  `- sqlite` `- libchromaprint` `- mediainfo` | List of Packages Required to install and run lidarr |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: lidarr_servers
      roles:
        - aaron-cole.ansible_role_lidarr


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole


