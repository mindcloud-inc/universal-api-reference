# Get Campaign Report with OptiMonk

Retrieves a campaign report from OptiMonk.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/{campaignId}`
- **Base URL:** `https://api.optimonk.com/v1`
- **Official documentation:** [Get Campaign Report](https://api.optimonk.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The OptiMonk campaign ID. |
| `groupBy` | query | `string` | no | Report grouping granularity. |
| `from` | query | `string` | no | Start date or datetime. |
| `to` | query | `string` | no | End date or datetime. |
