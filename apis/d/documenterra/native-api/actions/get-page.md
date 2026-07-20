# Get Page with Documenterra

Retrieves a page from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/articles/:topicId`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Get Page](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-stranitsy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Documenterra project or publication identifier. |
| `topicId` | path | `string` | yes | Documenterra page identifier. |
