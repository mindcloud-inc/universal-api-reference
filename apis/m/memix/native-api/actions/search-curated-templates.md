# Search Curated Templates with Memix

Finds curated templates in Memix search.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates/search`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional query used to narrow curated templates. |
| `limit` | query | `number` | no | Maximum number of templates to return. |
