# List Teams with SupportBee

Retrieves teams from SupportBee.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [List Teams](https://supportbee.com/docs/api/reference#tag/Teams/paths/~1teams/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `with_users` | query | `boolean` | no | If true, include team users. |
| `user` | query | `string` | no | Filter teams for a specific user or alias. |
