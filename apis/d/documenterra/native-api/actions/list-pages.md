# List Pages with Documenterra

Retrieves pages from a Documenterra project or publication.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/articles`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [List Pages](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-vsekh-stranits-proyekta-publikatsii)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Documenterra project or publication identifier. |
