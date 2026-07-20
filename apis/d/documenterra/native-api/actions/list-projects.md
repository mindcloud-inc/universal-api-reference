# List Projects with Documenterra

Retrieves projects and publications from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [List Projects](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-vsekh-proyektov-i-publikatsiy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | query | `string` | no | Optional parent project or publication identifier. |
| `types` | query | `string` | no | Optional comma-separated Documenterra project/publication types filter. |
