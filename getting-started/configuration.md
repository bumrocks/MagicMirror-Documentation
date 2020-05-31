# Configuration

## Raspberry Specific

The following wiki links are helpful for the initial configuration of your MagicMirror² operating system:
- [Configuring the Raspberry Pi](https://github.com/MichMich/MagicMirror/wiki/Configuring-the-Raspberry-Pi)
- [Auto Starting MagicMirror](https://github.com/MichMich/MagicMirror/wiki/Auto-Starting-MagicMirror)


## General

1. Copy `/home/pi/MagicMirror/config/config.js.sample` to `/home/pi/MagicMirror/config/config.js`. \
   **Note:** If you used the installer script. This step is already done for you.

2. Modify your required settings. \
   Note: You can check your configuration running `npm run config:check` in `/home/pi/MagicMirror`.


The following properties can be configured:

| **Option** | **Description** |
| --- | --- |
| `port` | The port on which the MagicMirror² server will run on. The default value is `8080`. |
| `address` | The *interface* ip address on which to accept connections. The default is `localhost`, which would prevent exposing the built-in webserver to machines on the local network. To expose it to other machines, use: `0.0.0.0`. |
| `ipWhitelist` | The list of IPs from which you are allowed to access the MagicMirror². The default value is `["127.0.0.1", "::ffff:127.0.0.1", "::1"]`, which is from `localhost` only. Add your IP when needed. You can also specify IP ranges with subnet masks (`["127.0.0.1", "127.0.0.1/24"]`) or directly with (`["127.0.0.1", ["192.168.0.1", "192.168.0.100"]]`). Set `[]` to allow all IP addresses. For more information see: [follow post ipWhitelist HowTo](https://forum.magicmirror.builders/topic/1326/ipwhitelist-howto) |
| `language` | The language of the interface. (Note: Not all elements will be localized.) Possible values are `en`, `nl`, `ru`, `fr`, etc., but the default value is `en`. |
| `timeFormat` | The form of time notation that will be used. Possible values are `12` or `24`. The default is `24`. |
| `units` | The units that will be used in the default weather modules. Possible values are `metric` or `imperial`. The default is `metric`. |
| `modules` | An array of active modules. **The array must contain objects. See [module configuration](/modules/configuration.md) for more information.** |
