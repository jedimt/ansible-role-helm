Ansible Role: Helm Install
=========

Installs Helm

Requirements
------------

Ansible >= 2.9

Linux Distribution

Debian Family

Debian

Stretch (9)
Buster (10)
Bullseye (11)
Ubuntu

Bionic (18.04)
Focal (20.04)

Role Variables
--------------

    # Temp directory for Helm download
    helm_download_dir: /tmp/helm

    # Helm version number
    helm_version: '3.11.1'

    # The CPU architecture of the Helm executable to install
    helm_architecture: 'amd64'

    # Mirror to download Helm from
    helm_mirror: 'https://get.helm.sh'

    # Dir where Helm should be installed
    helm_install_dir: '/usr/local/share/helm'

    # The OS of the Helm redistributable. This is 'linux' for Ubuntu/Debian
    helm_os: 'linux'

    # File name of the Helm redistributable file
    helm_filename: 'helm-v{{ helm_version }}-{{ helm_os }}-{{ helm_architecture }}.tar.gz'

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: jedimt.helm_install, helm_version: '3.11.1' }

License
-------

MIT

Author Information
------------------

Aaron Patten
aaronpatten@gmail.com

Adapted from https://github.com/gantsign/ansible_role_helm
