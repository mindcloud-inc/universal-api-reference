# List Notes with Belong

Retrieves all note entries from Belong.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes`
- **Base URL:** `https://api.belong.net/api/v3`
- **Official documentation:** [List Notes](https://api.belong.net/api/v3/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hubId` | query | `string` | no | — |
| `userId` | query | `string` | no | — |
| `search` | query | `string` | no | — |
| `take` | query | `number` | no | — |
| `skip` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
| `sort` | query | `list` | no | Accepted values: `Created At`, `Title`, `Updated At`. |
| `order` | query | `list` | no | Accepted values: `Ascending`, `Descending`. |
