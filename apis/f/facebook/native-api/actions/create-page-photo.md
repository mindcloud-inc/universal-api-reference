# Create Page Photo with Facebook

## Endpoint

- **Method:** `POST`
- **Path:** `/:pageId/photos`
- **Base URL:** `https://graph.facebook.com/v25.0`
- **Official documentation:** [Create Page Photo](https://developers.facebook.com/docs/graph-api/reference/page/photos/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `list<string>` | yes | — |
| `url` | body | `string` | yes | Public image URL. JPEG, BMP, PNG, GIF, or TIFF up to 10 MB. |
| `caption` | body | `string` | no | — |
| `published` | body | `boolean` | no | Set to false to upload without publishing. Unpublished photos are deleted after about 24 hours unless published. |
| `scheduled_publish_time` | body | `date` | no | Set Published to false when scheduling. |
