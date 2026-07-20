# Archive Media with Wistia

Archives one or more media items in Wistia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/modern/medias/archive`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Archive Media](https://docs.wistia.com/reference/put_medias-archive)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedIds[]` | body | `array<string>` | yes |
