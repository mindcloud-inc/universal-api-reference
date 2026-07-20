# Search Papers With AND Query with arXiv

Finds papers in arXiv using an AND query.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers With AND Query](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Boolean AND arXiv query string. |
