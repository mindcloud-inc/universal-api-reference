# Create Activity with Zixflow

Creates a new activity in Zixflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection-records/activity-list`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Create Activity](https://docs.zixflow.com/api-reference/activity-list/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iconType` | body | `string` | yes | Activity icon type. |
| `iconValue` | body | `string` | yes | Activity icon value. |
| `name` | body | `string` | yes | Activity name. |
| `scheduleAt` | body | `string` | yes | Scheduled timestamp for the activity. |
| `description` | body | `string` | no | Activity description. |
| `associated` | body | `string` | no | Associated record reference. |
| `status` | body | `string` | no | Activity status identifier. |
