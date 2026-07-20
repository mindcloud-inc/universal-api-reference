# Search Papers By Relevance Ascending with arXiv

Finds papers in arXiv by ascending relevance.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers By Relevance Ascending](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | arXiv query string to execute. |
