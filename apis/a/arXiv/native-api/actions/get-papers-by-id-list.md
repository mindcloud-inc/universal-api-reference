# Get Papers By ID List with arXiv

Retrieves papers from arXiv by ID list.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Get Papers By ID List](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_list` | query | `string` | yes | Required comma-separated arXiv paper IDs. |
