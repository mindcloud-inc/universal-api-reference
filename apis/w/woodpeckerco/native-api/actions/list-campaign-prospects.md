# List Campaign Prospects with Woodpecker.co

Retrieves prospects from a Woodpecker campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1/prospects`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [List Campaign Prospects](https://developers.woodpecker.co/docs/prospects/get-prospects-campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaigns_id` | query | `string` | yes | Comma-separated Woodpecker campaign IDs. Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | Page number. |
| `per_page` | query | `number` | no | Number of prospects per page. |
| `sort` | query | `string` | no | Woodpecker sort expression. |
