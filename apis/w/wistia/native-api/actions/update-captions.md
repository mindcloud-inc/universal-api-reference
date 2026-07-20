# Update Captions with Wistia

Updates captions for a Wistia media language.

## Endpoint

- **Method:** `PUT`
- **Path:** `/modern/medias/:mediaHashedId/captions/:languageCode`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Update Captions](https://docs.wistia.com/reference/put_medias-mediahashedid-captions-languagecode)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `languageCode` | path | `string` | yes |
| `text` | body | `string` | yes |
