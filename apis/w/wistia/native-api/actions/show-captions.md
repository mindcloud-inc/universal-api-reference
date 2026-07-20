# Show Captions with Wistia

Retrieves captions for a Wistia media in one language.

## Endpoint

- **Method:** `GET`
- **Path:** `/modern/medias/:mediaHashedId/captions/:languageCode`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Show Captions](https://docs.wistia.com/reference/get_medias-mediahashedid-captions-languagecode)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `languageCode` | path | `string` | yes |
