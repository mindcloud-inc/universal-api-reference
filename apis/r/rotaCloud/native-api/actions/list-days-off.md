# List Days Off with RotaCloud

Lists days off in RotaCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/days_off`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Days Off](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | — |
| `start` | query | `string` | yes | — |
| `users` | query | `number` | no | Send multiple values as a string separated by `,`. |
