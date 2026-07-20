# Search Notes with Histre

Finds notes in Histre by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/notes/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Search Notes](https://histre.com/features/api/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search query used to find matching Histre notes. |
| `page` | query | `number` | no | Optional page number for paginated Histre note search results. |
