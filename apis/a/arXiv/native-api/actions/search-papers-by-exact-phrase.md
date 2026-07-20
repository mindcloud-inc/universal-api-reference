# Search Papers By Exact Phrase with arXiv

Finds papers in arXiv by exact phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers By Exact Phrase](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Exact phrase arXiv query string. |
