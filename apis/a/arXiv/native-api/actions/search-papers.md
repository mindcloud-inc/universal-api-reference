# Search Papers with arXiv

Finds papers in arXiv by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Required arXiv search expression using the documented prefix syntax such as all:, ti:, au:, abs:, cat:, or submittedDate:[YYYYMMDDTTTT+TO+YYYYMMDDTTTT]. |
| `id_list` | query | `string` | no | Optional comma-separated arXiv IDs. When provided with Search Query, arXiv returns only IDs that also match the query. |
| `sortBy` | query | `list` | no | Optional arXiv sort field. Accepted values: `0`, `1`, `2`. |
| `sortOrder` | query | `list` | no | Optional arXiv sort direction. Accepted values: `0`, `1`. |
