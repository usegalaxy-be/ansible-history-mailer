## ansible-history-mailer

Ansible role for downloading and configuring the [history mailer](https://github.com/usegalaxy-au/history-mailer) to manage user histories on a Galaxy Instance. The History Mailer script was written by Simon Gladman @slugger70 and Thom Cuddihy @thomcuddihy.

### Role variables

See [defaults](defaults/main.yml)

Example configuration:

```
history_mailer_warn_days: 365
history_mailer_delete_days: 385
history_mailer_email_days_threshold: 20
history_mailer_purge_days_threshold: 14

history_mailer_galaxy_url: https://galaxy-cat.genome.edu.au
history_mailer_galaxy_api_key: 'aeee1234'

history_mailer_mail_base_url: https://mail.galaxy-cat.genome.edu.au/api/v1/
history_mailer_mail_api_key: 'xBBVeiBx'

history_mailer_cron_jobs:
- name: warn_and_delete
  weekday: "1"
  hour: "12"
  options:
    - production
    - warn
    - delete
- name: purge_histories
  weekday: "0"
  hour: "12"
  options:
    - production
    - purge
```

