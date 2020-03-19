# Ansible Role: `aisbergg.btrfsmaintenance`

This Ansible role installs and configures the [Btrfs Maintenance Scripts](https://github.com/kdave/btrfsmaintenance) on Linux systems.

## Requirements

The `btrfsmaintenance` scripts requires Systemd and so does this role.

## Role Variables

| Variable | Default | Comments |
|----------|---------|----------|
| `btrfsmaintenance_repository` | `https://github.com/kdave/btrfsmaintenance.git` | Repository to install from |
| `btrfsmaintenance_version` | `latest` | Version to install. The version can be specified as a specific value (e.g. '0.4.2') or set to 'latest', to fetch the latest released version. |
| `btrfsmaintenance_service_enabled` | `true` | Enable the btrfsmaintenance scripts to run periodically |
| `btrfsmaintenance_config` | `{}` | The configuration options for the `btrfsmaintenance` scripts. Detailed information can be found in the [files/btrfsmaintenance.j2](files/btrfsmaintenance.j2) file. |
| `btrfsmaintenance_config.log_output` | `journal` | Output target for messages. Valid options: none, stdout, journal, syslog |
| `btrfsmaintenance_config.defrag_paths` | `[]` | Run periodic defrag on selected paths |
| `btrfsmaintenance_config.defrag_period` | `none` | Frequency of defrag. Valid options: none, daily, weekly, monthly |
| `btrfsmaintenance_config.defrag_min_size` | `+1M` | Minimal file size to consider for defragmentation |
| `btrfsmaintenance_config.balance_mountpoints` | `["/"]` | Which mountpoints/filesystems to balance periodically |
| `btrfsmaintenance_config.balance_period` | `weekly` | Frequency of periodic balance. Valid options: none, daily, weekly, monthly |
| `btrfsmaintenance_config.balance_dusage` | `1 5 10 20 30 40 50` | The usage percent for balancing data block groups |
| `btrfsmaintenance_config.balance_musage` | `1 5 10 20 30` | The usage percent for balancing metadata block groups |
| `btrfsmaintenance_config.scrub_mountpoints` | `["/"]` | Which mountpoints/filesystems to scrub periodically. |
| `btrfsmaintenance_config.scrub_period` | `monthly` | Frequency of periodic scrub. Valid options: none, daily, weekly, monthly |
| `btrfsmaintenance_config.scrub_priority` | `idle` | Priority of IO at which the scrub process will run. Valid options: idle, normal |
| `btrfsmaintenance_config.scrub_read_only` | `false` | Do read-only scrub and don't try to repair anything. |
| `btrfsmaintenance_config.trim_period` | `none` | Frequency of periodic trim. Valid options: none, daily, weekly, monthly |
| `btrfsmaintenance_config.trim_mountpoints` | `["/"]` | Which mountpoints/filesystems to trim periodically. |
| `btrfsmaintenance_config.allow_concurrency` | `false` | Run the jobs in FIFO order when scheduled at overlapping times. |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  vars:
    btrfsmaintenance_version: latest
    btrfsmaintenance_config:
      defrag_paths:
        - "/"
        - "/home"
      defrag_period: monthly
  roles:
    - aisbergg.btrfsmaintenance
```

## License

MIT

## Author Information

Andre Lehmann (aisberg@posteo.de)
