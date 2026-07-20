# Delete Oncall Schedule with Pinghome

Deletes an existing on-call schedule from Pinghome.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/incident-cmd/v1/team/:id/schedule`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Delete Oncall Schedule](https://docs.pinghome.io/incident-management/incident-schedule-management/delete-oncall-schedule/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
| `team_member_id` | query | `string` | yes | The unique ID of the team member whose schedule is being deleted. |
| `created_at` | query | `string` | yes | The creation timestamp identifying the schedule. |
