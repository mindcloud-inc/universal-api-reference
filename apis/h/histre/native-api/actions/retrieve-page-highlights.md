# Retrieve Page Highlights with Histre

Retrieves page highlights from Histre.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/highlight/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Retrieve Page Highlights](https://histre.com/features/api/highlights/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | no | Page URL whose highlights should be retrieved. Provide this or Highlight ID. |
| `highlight_id` | query | `string` | no | Highlight identifier to retrieve. Provide this or URL. |
| `page` | query | `number` | no | Optional page number for paginated highlight retrieval. |
