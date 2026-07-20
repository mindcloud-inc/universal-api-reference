# List Sequence Recipients with Hunter

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/recipients`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [List Sequence Recipients](https://hunter.io/api-documentation/v2#list-recipients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Identifier of the sequence. |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
