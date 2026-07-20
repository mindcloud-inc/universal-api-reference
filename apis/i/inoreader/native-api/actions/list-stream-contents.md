# List Stream Contents with Inoreader

Retrieves contents from a specific Inoreader stream.

## Endpoint

- **Method:** `GET`
- **Path:** `/stream/contents/:streamId`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [List Stream Contents](https://www.inoreader.com/developers/stream-contents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `streamId` | path | `string` | yes | URL-encoded stream ID appended to the endpoint path. |
| `n` | query | `number` | no | Number of items to return. |
| `r` | query | `string` | no | Return newest first by default, or oldest first with o. |
| `ot` | query | `number` | no | Unix timestamp from which to begin fetching items. |
| `xt` | query | `string` | no | Exclude a target stream or state such as the read state. |
| `it` | query | `string` | no | Include only items matching a specific target label or state. |
| `c` | query | `string` | no | Continuation token from a previous response. |
| `includeAllDirectStreamIds` | query | `boolean` | no | Include automatically added folder tags in article categories. |
| `annotations` | query | `boolean` | no | Include your annotations for each article. |
| `summaries` | query | `boolean` | no | Include Inoreader Intelligence summaries for each article. |
