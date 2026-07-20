# List Recent Media with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `api/v2/media.json`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [List Recent Media](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional recent media filter value. |
| `per_page` | query | `number` | no | Number of results per page. |
| `user_id` | query | `string` | no | Optional comma-separated user IDs to filter recent media. |
