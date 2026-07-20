# Search Nodes with ACLU

Finds Torture Database nodes by keyword and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/searchnode/retrieve.json`
- **Base URL:** `https://www.thetorturedatabase.org/rest`
- **Official documentation:** [Search Nodes](https://www.thetorturedatabase.org/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keys` | query | `string` | yes | Search keywords exactly as documented. |
| `page` | query | `number` | no | Zero-based page number. |
| `filters` | query | `string` | no | Raw Solr filter string copied from the site URL after filters=. |
