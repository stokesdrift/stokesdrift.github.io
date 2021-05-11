---
title: "Configuration"
date: 2017-03-23
publishdate: 2017-03-24
weight: 20
menu_section: setup
---

In order to run your rack application within the drift server you will need to create a `drift_config.yml` file at the root of your project.

Here is a sample configuration file:

```yaml
server:
 port: 8888
 host: 127.0.0.1
apps:
 -
   app_file: config.ru
   name: "Example"
   url_path: "/"
```

The main parts of the configuration file is as follows:
* `server` - the server specific configurations
* `apps` - the apps that will run on this server and where they are located

The server section consists of:
* `host` - host binding for the server, typically you'll want to set this to `0.0.0.0`.
* `port` - the port the server should be running at

The apps section is a list of apps that are to run on the server, each app consists of:
* `app_file` - for typical rack apps set this to the rack config file `config.ru`, this could be different files in the future and will allow the server to adapt how it loads the app
* `name` - the name of the app
* `url_path` - the context path starting point of the app, set this to `/` if you don't want a prefix such as `/api/` 

[Next]({{< ref "Running" >}} "Running")