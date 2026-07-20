# Create Check with Pingdom

## Endpoint

- **Method:** `POST`
- **Path:** `/checks`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Create Check](https://docs.pingdom.com/api/#tag/Checks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Check name. |
| `host` | body | `string` | yes | Target host for the check. |
| `type` | body | `string` | yes | Type of check to create. |
| `paused` | body | `boolean` | no | Pause the check immediately after creation. |
| `resolution` | body | `number` | no | How often the check should run, in minutes. |
| `userids` | body | `string` | no | Comma-separated list of user identifiers to alert. |
| `sendnotificationwhendown` | body | `number` | no | Send a notification when the check has been down this many times. |
| `notifyagainevery` | body | `number` | no | Send another notification every n results. Use 0 to disable repeat notifications. |
| `notifywhenbackup` | body | `boolean` | no | Notify again when the check is back up. |
| `tags[]` | body | `array<string>` | no | Tags to assign to the check. |
| `probe_filters[]` | body | `array<string>` | no | Probe selection filters such as region filters. |
| `ipv6` | body | `boolean` | no | Use IPv6 instead of IPv4 when applicable. |
| `responsetime_threshold` | body | `number` | no | Response-time threshold in milliseconds that triggers a down alert. |
| `integrationids[]` | body | `array<number>` | no | Integration identifiers to associate with the check. |
| `teamids` | body | `string` | no | Comma-separated team identifiers to alert. |
| `custom_message` | body | `string` | no | Custom message appended to email and webhook alerts. |
