# Update Clip with HelpDocs

Updates an existing clip in HelpDocs.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/clip/:clip_id`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Update Clip](https://apidocs.helpdocs.io/article/yl1k6865rt-updating-a-clip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clip_id` | path | `string` | yes | Clip ID to update. |
| `content` | body | `string` | no | Updated clip content. |
| `title` | body | `string` | no | Updated clip title. |
