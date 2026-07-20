# List Daily Revenue with RotaCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/daily_revenue`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Daily Revenue](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | — |
| `locations` | query | `number` | no | Send multiple values as a string separated by `,`. |
| `start` | query | `string` | yes | — |
