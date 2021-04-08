# Fork of bitsensor/elastalert-kibana-plugin

The original bitsensor/elastalert-kibana-plugin repository has become mostly stale, with over 50 open issues. 

Consequently, it is difficult to merge fixes, dependency upgrades, and new features into bitsensor. Because of this, a fork of elastalert-kibana-plugin has been created.

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
- [Kibana 7.10.0～](https://github.com/nsano-rururu/elastalert-kibana-plugin/releases/tag/1.4.0)

## Installation
Check the [releases](https://github.com/nsano-rururu/elastalert-kibana-plugin/releases) page to download and install the latest version of this plugin that is compatible with your Kibana version. Please be aware that you will need a running ElastAlert server to make use of this plugin.

[ElastAlert Server Docker Images](https://github.com/nsano-rururu/elastalert-kibana-plugin/wiki/ElastAlert-Server-Docker-Images)
[docker-compose sample](https://github.com/nsano-rururu/elastalert-kibana-plugin/wiki/docker-compose-sample)

## Configuration

By default the plugin will connect to `http://localhost:3030`. If your ElastAlert server is running on a different host or port add/change the following options in your `config/kibana.yml` file: 

⚠️ from version 1.4.0 config section name has been changed:
`elastalert-kibana-plugin -> elastalertKibanaPlugin`

```
# 1.2.0, 1.3.0
elastalert-kibana-plugin.serverSsl: false
elastalert-kibana-plugin.serverHost: localhost
elastalert-kibana-plugin.serverPort: 3030

# 1.4.0
elastalertKibanaPlugin.serverSsl: false
elastalertKibanaPlugin.serverHost: localhost
elastalertKibanaPlugin.serverPort: 3030
```
### Dev notes

If you would like to run this plugin:

1) Clone kibana repo: `git clone https://github.com/elastic/kibana.git` and enter to repo: `cd kibana`
2) Change branch: `git checkout 7.11`
3) Install nvm if you don't have
4) Install node: `nvm install $(cat .nvmrc)`
5) Configure node: `nvm use $(cat .nvmrc)`
6) Install yarn: `npm install -g yarn`
7) Run: `yarn kbn bootstrap`
8) Configure kibana (`config/kibana.yml`):

```
elastalertKibanaPlugin.serverSsl: false
elastalertKibanaPlugin.serverHost: localhost
elastalertKibanaPlugin.serverPort: 8030
logging.verbose: true
```

10) Clone this repo to: `plugins/`. `git clone https://github.com/nsano-rururu/elastalert-kibana-plugin.git plugins/elastalert-kibana-plugin`
11) Run elastic with elastalert. For test purpose you can use: `plugins/elastalert-kibana-plugin/dev/elastic-dev-env/docker-compose.yml` be running:

`docker-compose -p elastic-dev-env -f dev\elastic-dev-env\docker-compose.yml up -d`

12) Run kibana: `yarn start --oss`

## Contribution
Please report any issues or suggestions you have on the [issues page](https://github.com/nsano-rururu/elastalert-kibana-plugin/issues). If you want to create a pull request please check our [contribution guide](CONTRIBUTING.md).
