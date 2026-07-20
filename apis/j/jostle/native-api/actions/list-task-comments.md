# List Task Comments with Jostle

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tasks/task/:id/comments`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [List Task Comments](https://api.jostle.me/reference/gettaskcommentslist-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id of the task |
| `count` | query | `string` | no | Maximum number of results to return per page |
| `offset` | query | `string` | no | Offset to receive additional pages of content |
