# List Recently Submitted Papers with arXiv

Lists recently submitted papers in arXiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [List Recently Submitted Papers](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Optional arXiv search expression. Use all:<term> for broad matching before sorting by submittedDate. |
