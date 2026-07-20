# Search for Collections with Histre

Finds collections in Histre by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/collections/search/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Search for Collections](https://histre.com/features/api/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | All or part of the collection title to search for. |
| `url` | query | `string` | no | Optional URL to include collection association information in the results. |
| `channel` | query | `string` | no | Optional request source channel. Histre docs allow extension or web. |
