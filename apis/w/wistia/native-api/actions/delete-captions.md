# Delete Captions with Wistia

Deletes captions for a Wistia media language.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/modern/medias/:mediaHashedId/captions/:languageCode`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Delete Captions](https://docs.wistia.com/reference/delete_medias-mediahashedid-captions-languagecode)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `languageCode` | path | `string` | yes |
