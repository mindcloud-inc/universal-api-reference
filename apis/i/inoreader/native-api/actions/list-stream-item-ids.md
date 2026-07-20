# List Stream Item IDs with Inoreader

Retrieves item IDs from an Inoreader stream.

## Endpoint

- **Method:** `GET`
- **Path:** `/stream/items/ids`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [List Stream Item IDs](https://www.inoreader.com/developers/item-ids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Stream ID to fetch item IDs from. |
| `n` | query | `number` | no | Number of item IDs to return. |
| `r` | query | `string` | no | Return newest first by default, or oldest first with o. |
| `ot` | query | `number` | no | Unix timestamp from which to begin fetching item IDs. |
| `xt` | query | `string` | no | Exclude a target stream or state such as the read state. |
| `it` | query | `string` | no | Include only item IDs matching a specific target label or state. |
| `c` | query | `string` | no | Continuation token from a previous response. |
| `includeAllDirectStreamIds` | query | `boolean` | no | Include automatically added folder tags in direct stream IDs. |
