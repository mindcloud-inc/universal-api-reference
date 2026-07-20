# Filter ID List By Search Query with arXiv

Finds arXiv papers from an ID list matching a query.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Filter ID List By Search Query](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Full arXiv search expression used to filter the provided ID list. |
| `id_list` | query | `string` | yes | Comma-separated arXiv paper IDs to filter. |
