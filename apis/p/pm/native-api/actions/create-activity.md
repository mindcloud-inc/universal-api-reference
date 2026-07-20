# Create Activity with 5pm

Creates a new activity in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/activity/add`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Create Activity](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activity[taskId]` | query | `string` | yes | Task identifier for the activity. |
| `activity[text]` | query | `string` | yes | Text body of the activity. |
| `activity[type]` | query | `string` | yes | Activity type such as msg or progress. |
