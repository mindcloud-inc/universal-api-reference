# Update Studio Caption with Restream

Updates a studio caption in Restream.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/user/studio/captions/:captionId`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Update Studio Caption](https://developers.restream.io/studio/studio-caption-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `captionId` | path | `string` | yes | The ID of the caption to update. |
| `secondaryText` | body | `string` | no | Updated caption secondary text. |
| `text` | body | `string` | no | Updated caption text. |
