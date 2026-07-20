# List Activity Comments with Strava

Retrieves comments for a Strava activity.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/:id/comments`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [List Activity Comments](https://developers.strava.com/docs/reference/#api-Activities-getCommentsByActivityId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the activity whose comments are requested. |
| `per_page` | query | `number` | no | Number of comments to return per page (1-200). |
| `page` | query | `number` | no | Page number to return, starting at 1. |
