# Get Entry with Feedbin

Retrieves a single entry from Feedbin.

## Endpoint

- **Method:** `GET`
- **Path:** `entries/[:id].json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Get Entry](https://github.com/feedbin/feedbin-api/blob/master/content/entries.md#get-v2entries3648json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feedbin entry ID. |
| `include_original` | query | `boolean` | no | Include original entry data if the entry has been updated. |
| `include_enclosure` | query | `boolean` | no | Include podcast/RSS enclosure data. |
| `include_content_diff` | query | `boolean` | no | Include an HTML diff of changed content. |
