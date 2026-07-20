# Translate Media with Wistia

Translates the transcript for a Wistia media item.

## Endpoint

- **Method:** `POST`
- **Path:** `/modern/medias/:mediaHashedId/translate`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Translate Media](https://docs.wistia.com/reference/post_medias-mediahashedid-translate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `language` | body | `string` | no |
