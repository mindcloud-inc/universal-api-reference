# Update Check with Pingdom

## Endpoint

- **Method:** `PUT`
- **Path:** `/checks/:checkid`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Update Check](https://docs.pingdom.com/api/#tag/Checks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkid` | path | `number` | yes | Identifier of the check to update. |
| `name` | body | `string` | no | Updated check name. |
| `host` | body | `string` | no | Updated target host. |
| `paused` | body | `boolean` | no | Pause or unpause the check. |
| `resolution` | body | `number` | no | Updated check interval in minutes. |
| `userids` | body | `string` | no | Comma-separated list of user identifiers to alert. |
| `sendnotificationwhendown` | body | `number` | no | Send a notification when the check has been down this many times. |
| `notifyagainevery` | body | `number` | no | Send another notification every n results. Use 0 to disable repeat notifications. |
| `notifywhenbackup` | body | `boolean` | no | Notify again when the check is back up. |
| `tags[]` | body | `array<string>` | no | Replace the check tags with this list. |
| `addtags[]` | body | `array<string>` | no | Tags to add without replacing the current tag list. |
| `probe_filters[]` | body | `array<string>` | no | Updated probe selection filters such as region filters. |
| `ipv6` | body | `boolean` | no | Use IPv6 instead of IPv4 when applicable. |
| `responsetime_threshold` | body | `number` | no | Response-time threshold in milliseconds that triggers a down alert. |
| `integrationids[]` | body | `array<number>` | no | Integration identifiers to associate with the check. |
| `teamids` | body | `string` | no | Comma-separated team identifiers to alert. |
| `custom_message` | body | `string` | no | Custom message appended to email and webhook alerts. |
