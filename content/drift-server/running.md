---
title: "Running"
date: 2017-03-23
publishdate: 2017-03-24
weight: 30
menu_section: setup
---

In your project root directory run:

`stokesdrift`

By default it runs the server on port `8888`, open a browser and go to [http://localhost:8888](http://localhost:8888).

If you want to test something from the stokesdrift github project you can run `run STOKES_DRIFT_OPTS="-r src/test/resources/examples" gradle run`. Where `src/test/resources/examples` is your ruby project folder.

Alternatively, you can run it in docker. To make a docker container, see [Example Project](https://github.com/stokesdrift/example-sinatra) for an example on doing this.
