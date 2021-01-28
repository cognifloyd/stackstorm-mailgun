# Mailgun integration pack

Pack which allows integration with [Mailgun](https://mailgun.com) service.

## Configuration

Copy the example configuration in [mailgun.yaml.example](./mailgun.yaml.example)
to `/opt/stackstorm/configs/mailgun.yaml` and edit as required.

It must contain:

* ``domain`` - Your mailgun domain (e.g. ``myuser.mailgun.org``)
* ``api_key`` - Your mailgun API key.

You can also use dynamic values from the datastore. See the
[docs](https://docs.stackstorm.com/reference/pack_configs.html) for more info.

**Note** : When modifying the configuration in `/opt/stackstorm/configs/` please
           remember to tell StackStorm to load these new values by running
           `st2ctl reload --register-configs`

## Actions

* ``send_email`` - Send email via Mailgun HTTP API.
