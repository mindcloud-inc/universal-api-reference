# List Availability with RotaCloud

Retrieves availability from RotaCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/availability`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Availability](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | — |
| `start` | query | `string` | yes | — |
| `users` | query | `number` | no | Send multiple values as a string separated by `,`. |
