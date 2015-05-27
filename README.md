# data.gov.ro

[data.gov.ro](http://data.gov.ro) is the Romanian national portal for open data.

## Setup

`vagrant up` will provision a Vagrant machine using Ansible, with a CKAN 2.3
[installation](http://docs.ckan.org/en/ckan-2.3/maintaining/installing/install-from-source.html)
from source. Use `supervisorctl` to control the `ckan` process.

## Folder hierarchy

- `ckan/`
  - `etc/` - symlinked to `/etc/ckan`, contains the configuration file
  - `lib/` - symlinked to `/usr/lib/ckan`, contains CKAN code
    - `default/src/ckanext-romania_theme/` - code for our custom theme
      - `i18n/ro/` - custom translations
- `docs/`
- `provisioning/playbook.yml` - provisioning Ansible script

Logs are in `/var/log/supervisor`.
