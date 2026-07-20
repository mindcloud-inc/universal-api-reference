# List Related Hubs with Belong

Retrieves related hubs from Belong by hub ID or slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/hubs/:id/related`
- **Base URL:** `https://api.belong.net/api/v3`
- **Official documentation:** [List Related Hubs](https://api.belong.net/api/v3/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `withMarkers` | query | `boolean` | no |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
| `cursor` | query | `string` | no |
