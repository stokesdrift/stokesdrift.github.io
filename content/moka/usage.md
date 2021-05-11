---
title: "Usage"
date: 2017-03-23
publishdate: 2017-03-24
weight: 20
menu_section: setup
---


The idea behind moka is to provide a way to override property file defaults with environment variables passed to the application.

For instance, take this example property file:

```yaml
my.property=defaultfordev
```

And say its located under `src/java/resources/config` called `app.properties`.

In your java code you would init your config with moka via:

```java
Configuration config = new Configuration("app");
config.addLoadPath("/config");
config.init();
```

And at runtime if you wanted to override the value with an environment variable you would run `export MY_PROPERTY=propertyforprod`.

This would override the property value with `propertyforprod`.

To get this property in your code you would use:

```java
config.getString("my.property");
```	

In addition to environment variable overrides it supports system property eg (-Dmy.property=blah) overrides.

The supported property values are:
* Integer - `config.getInteger("my.int")` this would parse a string into an integer
* String - `config.getString("my.str")`
* String Array - `config.getStringArray("my.stringarr")` this would parse a comma delimited string value into a string array