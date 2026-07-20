# Search Papers With Submitted Date Filter with arXiv

Finds papers in arXiv by submitted date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://export.arxiv.org/api`
- **Official documentation:** [Search Papers With Submitted Date Filter](https://info.arxiv.org/help/api/user-manual.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | yes | Required full search expression that includes the submittedDate filter, for example au:del_maestro AND submittedDate:[202301010600+TO+202401010600]. |
