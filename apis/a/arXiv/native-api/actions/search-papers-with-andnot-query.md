# Search Papers With ANDNOT Query with arXiv

Finds papers in arXiv using an ANDNOT query.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers With ANDNOT Query](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Boolean ANDNOT arXiv query string. |
