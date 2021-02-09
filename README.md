# balena-nginx-proxy-manager

[Nginx Proxy Manager](https://nginxproxymanager.com/) stack for balenaCloud

## Requirements

- Raspberry Pi 4 or a similar x64 device supported by BalenaCloud

## Getting Started

You can one-click-deploy this project to balena using the button below:

[![deploy-with-balena](https://balena.io/deploy.png)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/klutchell/balena-nginx-proxy-manager&defaultDeviceType=raspberrypi4-64)

## Manual Deployment

Alternatively, deployment can be carried out by manually creating a [balenaCloud account](https://dashboard.balena-cloud.com) and application, flashing a device, downloading the project and pushing it via either Git or the [balena CLI](https://github.com/balena-io/balena-cli).

### Application Environment Variables

Application envionment variables apply to all services within the application, and can be applied fleet-wide to apply to multiple devices.

|Name|Example|Purpose|
|---|---|---|
|`MYSQL_ROOT_PASSWORD`|`mysecretpassword`|password that will be set for the MariaDB root account|

## Usage

### proxy

<https://nginxproxymanager.com/>

When your docker container is running, connect to it on port `81` for the admin interface. Sometimes this can take a little bit because of the entropy of keys.

Default Admin User:

```
Email:    admin@example.com
Password: changeme
```

### duplicati

<https://docs.duplicati.com>

The most convenient way to configure and control Duplicati is using the Graphical User Interface. Duplicati provides an internal web server that allows the user to configure and schedule backup jobs, perform restore operations and apply settings. This web interface is available when Duplicati.Server.exe and/or Duplicati.GUI.TrayIcon.exe is/are running. The first instance of the web server is listening on TCP port `8200`.

## Contributing

Please open an issue or submit a pull request with any features, fixes, or changes.

## References

- <https://nginxproxymanager.com/>
- <https://docs.duplicati.com>

## License

[MIT License](./LICENSE)
