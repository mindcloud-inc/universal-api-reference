# Update Activity with Zixflow

Updates an existing activity in Zixflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collection-records/activity-list/:activityId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Update Activity](https://docs.zixflow.com/api-reference/activity-list/edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | path | `string` | yes | Activity identifier. |
| `iconType` | body | `string` | no | Activity icon type. |
| `iconValue` | body | `string` | no | Activity icon value. |
| `name` | body | `string` | no | Activity name. |
| `scheduleAt` | body | `string` | no | Scheduled timestamp for the activity. |
| `description` | body | `string` | no | Activity description. |
| `associated` | body | `string` | no | Associated record reference. |
| `status` | body | `string` | no | Activity status identifier. |
