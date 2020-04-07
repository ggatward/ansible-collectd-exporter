# Ansible Role: collectd_exporter

## Description

Deploy prometheus [collectd_exporter](https://github.com/prometheus/collectd_exporter) using ansible.

## Requirements

- Ansible >= 2.7 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `collectd_exporter_version` | 0.4.0 | collectd_exporter package version |
| `collectd_exporter_web_listen_address` | "0.0.0.0:9103" | Address on which collectd_exporter will listen |
| `collectd_exporter_config_flags_extra` | {} | Additional configuration flags passed at startup to collectd_exporter binary |

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - collectd_exporter
```
