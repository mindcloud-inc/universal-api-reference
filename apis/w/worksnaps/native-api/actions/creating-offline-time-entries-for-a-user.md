# Creating offline time entries for a user with Worksnaps

Creates offline time entries for a user in Worksnaps.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/users/{user_id}/time_entries.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Creating offline time entries for a user](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project |
| `user_id` | path | `string` | no | ID of the target user |
