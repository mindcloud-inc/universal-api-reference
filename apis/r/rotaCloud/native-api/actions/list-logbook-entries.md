# List Logbook Entries with RotaCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/logbook/user/:userId`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Logbook Entries](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Filter entries by ISO 8601 date. |
| `userId` | path | `number` | yes | — |
