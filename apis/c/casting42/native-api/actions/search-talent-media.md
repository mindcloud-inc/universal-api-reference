# Search Talent Media with Casting42

Finds talent media in Casting42 by talent tag.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/talents/media/find`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [Search Talent Media](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `talentTags[]` | body | `array<string>` | yes | Array of talent tags to search media for. |
| `attachmentLabels[]` | body | `array<number>` | no | Optional array of attachment label IDs. |
| `mediaType` | body | `string` | no | Media type filter, such as audio_files. |
| `mediaLang` | body | `string` | no | Optional media language filter. |
