# Search Artifacts with Chatvolt AI

Searches artifacts in Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/search`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Search Artifacts](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search term for name, description, or category name. Ignored if `ids` is present. |
| `ids[]` | query | `array<string>` | no | List of specific Artifact IDs (e.g., `id1,id2`). Overrides textual search. |
| `minPrice` | query | `number` | no | Minimum price filter. |
| `maxPrice` | query | `number` | no | Maximum price filter. |
| `categoryIds[]` | query | `array<string>` | no | List of category IDs. Includes sub-categories automatically. |
| `mediaTypes[]` | query | `array<string>` | no | Filter by media types (e.g., `IMAGE,VIDEO`). |
| `maxMedias` | query | `number` | no | Max number of media items to return per artifact. |
| `includeInactive` | query | `boolean` | no | If true, returns inactive artifacts as well. |
| `limit` | query | `number` | no | Pagination limit. |
| `page` | query | `number` | no | Pagination page number. |
