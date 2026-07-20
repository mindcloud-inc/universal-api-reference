# Update Task with Confluence

Updates an existing task in Confluence.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/tasks/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Update Task](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-task/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the task. |
| `status` | body | `string` | yes | Set the task to complete or incomplete. |
