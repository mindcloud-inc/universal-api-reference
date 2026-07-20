# List Entries with Feedbin

Retrieves a list of entries from Feedbin.

## Endpoint

- **Method:** `GET`
- **Path:** `entries.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [List Entries](https://github.com/feedbin/feedbin-api/blob/master/content/entries.md#get-v2entriesjson)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | no | Return entries created after this ISO 8601 timestamp. |
| `ids` | query | `string` | no | Comma-separated entry IDs. Feedbin allows up to 100 IDs per request. |
| `read` | query | `boolean` | no | Filter entries by read state. |
| `starred` | query | `boolean` | no | Filter entries by starred state. |
| `mode` | query | `string` | no | Use extended to include additional entry metadata. |
| `include_original` | query | `boolean` | no | Include original entry data if the entry has been updated. |
| `include_enclosure` | query | `boolean` | no | Include podcast/RSS enclosure data. |
| `include_content_diff` | query | `boolean` | no | Include an HTML diff of changed content. |
