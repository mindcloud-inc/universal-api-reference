# Get Feedback with zipBoard

Retrieves feedback comments from zipBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/comments`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Get Feedback](https://help.zipboard.co/article/182-api-for-issues-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileid` | body | `string` | no | Optional file ID whose feedback should be fetched. |
| `projectid` | body | `string` | no | Optional project ID whose feedback should be fetched. |
| `projectid` | query | `string` | yes | — |
