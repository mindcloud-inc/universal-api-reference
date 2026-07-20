# Search Pages with Tettra

Finds pages in Tettra by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/85329/search`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Search Pages](https://support.tettra.com/api-overview/api-endpoint-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Search term. Leave empty to return recent pages. |
