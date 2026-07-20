# List Storage RIDs with Crawlbase

Retrieves storage record IDs from Crawlbase.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/rids`
- **Base URL:** `https://api.crawlbase.com`
- **Official documentation:** [List Storage RIDs](https://crawlbase.com/docs/cloud-storage/rids/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of storage RIDs to return. |
| `scroll` | query | `boolean` | no | Use Crawlbase scroll mode for paginated RID retrieval. |
| `scroll_id` | query | `string` | no | Scroll identifier returned by a previous storage RIDs request. |
| `scroll_order` | query | `list` | no | RID scroll order. Accepted values: `0`, `1`. |
