# Search Templates By Query with Memix

Finds templates in Memix by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates/search`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search query for discovering templates. |
| `limit` | query | `number` | no | Maximum number of templates to return. |
