# Delete Multiple Pages with Documenterra

Deletes multiple pages from Documenterra.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:id/articles`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Delete Multiple Pages](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-udaleniye-neskolkikh-stranits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Documenterra project or publication identifier. |
| `ids[]` | body | `array<string>` | yes | Page identifiers to delete. |
