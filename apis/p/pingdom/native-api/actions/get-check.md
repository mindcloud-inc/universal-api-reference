# Get Check with Pingdom

## Endpoint

- **Method:** `GET`
- **Path:** `/checks/:checkid`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Get Check](https://docs.pingdom.com/api/#tag/Checks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkid` | path | `number` | yes | Identifier of the check to retrieve. |
| `include_teams` | query | `boolean` | no | Include team connections for the check. |
