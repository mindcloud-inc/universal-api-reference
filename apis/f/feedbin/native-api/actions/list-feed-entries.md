# List Feed Entries with Feedbin

Retrieves entries for a specific feed from Feedbin.

## Endpoint

- **Method:** `GET`
- **Path:** `feeds/[:feed_id]/entries.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [List Feed Entries](https://github.com/feedbin/feedbin-api/blob/master/content/entries.md#get-v2feeds203entriesjson)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_id` | path | `number` | yes | Feedbin feed ID. |
| `since` | query | `date` | no | Return entries created after this ISO 8601 timestamp. |
| `read` | query | `boolean` | no | Filter entries by read state. |
| `starred` | query | `boolean` | no | Filter entries by starred state. |
| `mode` | query | `string` | no | Use extended to include additional entry metadata. |
| `include_original` | query | `boolean` | no | Include original entry data if the entry has been updated. |
| `include_enclosure` | query | `boolean` | no | Include podcast/RSS enclosure data. |
| `include_content_diff` | query | `boolean` | no | Include an HTML diff of changed content. |
