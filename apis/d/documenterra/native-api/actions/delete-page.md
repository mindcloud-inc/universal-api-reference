# Delete Page with Documenterra

Deletes an existing page from Documenterra.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:id/articles/:topicId`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Delete Page](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-udaleniye-stranitsy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Documenterra project or publication identifier. |
| `topicId` | path | `string` | yes | Documenterra page identifier. |
