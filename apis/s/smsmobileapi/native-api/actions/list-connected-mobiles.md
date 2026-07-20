# List Connected Mobiles with Smsmobileapi

Retrieves connected gateway mobiles from Smsmobileapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/gateway/mobile/list/`
- **Base URL:** `https://api.smsmobileapi.com`
- **Official documentation:** [List Connected Mobiles](https://smsmobileapi.com/doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sid` | query | `string` | no | Filter the result to one exact connected mobile SID. |
| `search` | query | `string` | no | Search connected mobile fields such as SID, date, battery, version, or label. |
