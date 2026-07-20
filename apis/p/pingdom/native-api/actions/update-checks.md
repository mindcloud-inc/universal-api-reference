# Update Checks with Pingdom

## Endpoint

- **Method:** `PUT`
- **Path:** `/checks`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Update Checks](https://docs.pingdom.com/api/#tag/Checks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paused` | body | `boolean` | no | Pause or unpause the selected checks. |
| `resolution` | body | `number` | no | How often the selected checks should run, in minutes. |
| `checkids` | body | `string` | no | Comma-separated list of check identifiers to update. Defaults to all checks when omitted. |
