# Search Papers By Title with arXiv

Finds papers in arXiv by title.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers By Title](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Title search expression using the ti: prefix, for example ti:transformer. |
