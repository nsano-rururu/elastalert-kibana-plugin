# Fork of bitsensor/elastalert-kibana-plugin

The original bitsensor/elastalert-kibana-plugin repository has become mostly stale, with over 50 open issues. Consequently, it is difficult to merge fixes, dependency upgrades, and new features into bitsensor. Because of this, a fork of elastalert-kibana-plugin has been created. 

---

> This plugin provides a way to create, test and edit ElastAlert rules within Kibana.

![GitHub release](https://img.shields.io/github/release/nsano-rururu/elastalert-kibana-plugin.svg)
![Github Releases](https://img.shields.io/github/downloads/nsano-rururu/elastalert-kibana-plugin/total.svg)
![GitHub stars](https://img.shields.io/github/stars/nsano-rururu/elastalert-kibana-plugin.svg?style=social&label=Stars)

---

## Demo
![Showcase](showcase.gif)

## Requirements
- Our [ElastAlert server](https://github.com/bitsensor/elastalert) fork
- [Kibana 6.8.1～6.8.12、7.5.1～7.8.1](https://github.com/nsano-rururu/elastalert-kibana-plugin/releases/tag/1.2.0)
- [Kibana 7.9.0～7.9.3](https://github.com/nsano-rururu/elastalert-kibana-plugin/releases/tag/1.3.0)
- Does not support kibana 7.10 or higher

## Installation
Check the [releases](https://github.com/nsano-rururu/elastalert-kibana-plugin/releases) page to download and install the latest version of this plugin that is compatible with your Kibana version. Please be aware that you will need a running ElastAlert server to make use of this plugin.

[ElastAlert Server Docker Images](https://github.com/nsano-rururu/elastalert-kibana-plugin/wiki/ElastAlert-Server-Docker-Images)<br>
[docker-compose sample](https://github.com/nsano-rururu/elastalert-kibana-plugin/wiki/docker-compose-sample)

## Configuration
By default the plugin will connect to `localhost:3030`. If your ElastAlert server is running on a different host or port add/change the following options in your `config/kibana.yml` file: 

```
elastalert-kibana-plugin.serverHost: 123.0.0.1
elastalert-kibana-plugin.serverPort: 9000
```

## Contribution
Please report any issues or suggestions you have on the [discussions page](https://github.com/nsano-rururu/elastalert-kibana-plugin/discussions). If you want to create a pull request please check our [contribution guide](CONTRIBUTING.md).
