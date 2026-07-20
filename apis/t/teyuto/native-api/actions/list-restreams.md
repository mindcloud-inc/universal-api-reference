# List Restreams with Teyuto

Retrieves all restreams from a Teyuto channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/restreams`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [List Restreams](https://docs.teyuto.com/api/get-list-of-restreams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page of restreams to return. |
| `page_size` | query | `number` | no | Number of restreams per page. |
| `search` | query | `string` | no | Search restreams by ID or name. |
| `order` | query | `string` | no | Sort order for restream results. |
| `livenow` | query | `boolean` | no | Return only restreams that are live right now. |
