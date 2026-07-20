# List Media with Speak Ai

Retrieves media from Speak Ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/media`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [List Media](https://docs.speakai.co/#8f14b0e6-7d40-40eb-8ea7-328943326e3b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaType` | query | `string` | no | Filter media by type such as audio or video. |
| `filterMedia` | query | `string` | no | Filter the list using Speak Ai's media filter value. |
| `filterName` | query | `string` | no | Filter media by name. |
| `folderId` | query | `string` | no | Restrict the list to media inside a specific folder. |
