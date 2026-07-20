# Typeahead Search with Strale

Finds capabilities or solutions in Strale by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/suggest/typeahead`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Typeahead Search](https://strale.dev/docs#api-suggest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geo` | query | `string` | no | Optional geography filter. |
| `limit` | query | `number` | no | Maximum number of results to return. |
| `q` | query | `string` | yes | Search query. |
| `type` | query | `string` | no | Restrict results to capabilities or solutions. |
