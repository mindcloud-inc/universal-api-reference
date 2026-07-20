# Attach Files with 5pm

Uploads files to an activity in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/activity/attachFiles`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Attach Files](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Unique identifier of the activity. |
