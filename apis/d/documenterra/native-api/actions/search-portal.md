# Search Portal with Documenterra

Finds portal content in Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Search Portal](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-poisk-po-portalu)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of search results to return. |
| `isReturnSnippets` | query | `number` | no | Whether to include result snippets. |
| `lang` | query | `string` | no | Optional portal language code for search results. |
| `projectIds` | query | `string` | no | Optional comma-separated project identifiers to scope the search. |
| `q` | query | `string` | yes | Search text. |
