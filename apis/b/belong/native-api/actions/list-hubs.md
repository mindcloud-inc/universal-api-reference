# List Hubs with Belong

Retrieves all available hubs from Belong.

## Endpoint

- **Method:** `GET`
- **Path:** `/hubs`
- **Base URL:** `https://api.belong.net/api/v3`
- **Official documentation:** [List Hubs](https://api.belong.net/api/v3/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hubType` | query | `list` | no | Accepted values: `Group`, `NFT Collection`. |
| `status` | query | `list` | no | Accepted values: `Incomplete`, `Published`. |
| `source` | query | `list` | no | Accepted values: `API`, `App`, `External`, `MCP`. |
| `private` | query | `boolean` | no | — |
| `ownerId` | query | `string` | no | — |
| `memberId` | query | `string` | no | — |
| `search` | query | `string` | no | — |
| `sort` | query | `list` | no | Accepted values: `Created At`, `Updated At`. |
| `order` | query | `list` | no | Accepted values: `Ascending`, `Descending`. |
| `fields[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | — |
| `limit` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
