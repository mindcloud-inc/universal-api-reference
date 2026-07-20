# List Recently Submitted Papers Ascending with arXiv

Lists recently submitted arXiv papers oldest first.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [List Recently Submitted Papers Ascending](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Optional arXiv query string to narrow submitted papers. |
