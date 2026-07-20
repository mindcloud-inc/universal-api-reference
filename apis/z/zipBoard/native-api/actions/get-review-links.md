# Get Review Links with zipBoard

Retrieves review links from zipBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/shareurl`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Get Review Links](https://help.zipboard.co/article/180-api-for-review-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileid` | body | `string` | no | Optional file ID to fetch review links for. |
| `projectid` | body | `string` | no | Optional project ID to fetch review links for. |
| `projectid` | query | `string` | yes | — |
