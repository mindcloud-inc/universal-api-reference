# Search Papers With Boolean Query with arXiv

Finds papers in arXiv using a Boolean query.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers With Boolean Query](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Full boolean arXiv search expression combining prefixes with AND, OR, and ANDNOT. |
