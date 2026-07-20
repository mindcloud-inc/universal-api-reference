# Get Paper By ID with arXiv

Retrieves a paper from arXiv by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Get Paper By ID](https://info.arxiv.org/help/api/user-manual.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_list` | query | `string` | yes | Required single arXiv paper ID, for example 2501.01234 or cs/9901001. |
