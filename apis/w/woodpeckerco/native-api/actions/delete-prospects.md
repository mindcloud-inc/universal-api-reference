# Delete Prospects with Woodpecker.co

Deletes prospects from Woodpecker or removes them from campaigns.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/v1/prospects`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Delete Prospects](https://developers.woodpecker.co/docs/prospects/DELETE-prospects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaigns_id` | query | `string` | no | Campaign IDs to remove the prospects from without deleting them globally. Send multiple values as a string separated by `,`. |
| `id` | query | `string` | yes | Comma-separated Woodpecker prospect IDs to delete. Send multiple values as a string separated by `,`. |
