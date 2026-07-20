# Search Papers By Category with arXiv

Finds papers in arXiv by category.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers By Category](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Category search expression using the cat: prefix, for example cat:cs.LG. |
