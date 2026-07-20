# Search for Highlights with Histre

Finds highlights in Histre by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/highlight/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Search for Highlights](https://histre.com/features/api/highlights/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search query used to find matching highlights. |
| `url` | query | `string` | no | Optional page URL to scope highlight search. |
| `page` | query | `number` | no | Optional page number for paginated highlight search results. |
