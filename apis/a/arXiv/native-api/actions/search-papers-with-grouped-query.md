# Search Papers With Grouped Query with arXiv

Finds papers in arXiv using a grouped query.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers With Grouped Query](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Grouped arXiv query string. |
