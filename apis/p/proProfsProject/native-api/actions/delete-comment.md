# Delete Comment with ProProfs Project

Deletes an existing comment from ProProfs Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/comments/{{comment_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Delete Comment](https://help.proprofsproject.com/managing-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | The comment ID to delete. |
