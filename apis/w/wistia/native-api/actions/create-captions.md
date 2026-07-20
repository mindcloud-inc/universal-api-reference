# Create Captions with Wistia

Adds captions to a Wistia media item.

## Endpoint

- **Method:** `POST`
- **Path:** `/modern/medias/:mediaHashedId/captions`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Create Captions](https://docs.wistia.com/reference/post_medias-mediahashedid-captions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `language` | body | `string` | yes |
| `text` | body | `string` | yes |
