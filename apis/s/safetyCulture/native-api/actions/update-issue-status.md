# Update Issue Status with SafetyCulture

Updates an issue status in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/v1/incidents/{task_id}/status`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Update Issue Status](https://developer.safetyculture.com/reference/incidentsservice_updatestatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Required. The ID of the action or issue you're updating. |
| `status_id` | body | `string` | yes | Required. The ID of the status you're updating the action or issue to. An issue can be in an "Open" or "Resolved" status, where each status is represented by hardcoded UUID values. Issue statuses: - Open: `547ed646-5e34-4732-bb54-a199d304368a`. - Resolved: `450484b1-56cd-4784-9b49-a3cf97d0c0ad`.  An action can be in a "To do", "In progress", "Complete", or "Can't do" status, where each status is represented by hardcoded UUID values. Action statuses: - To do: `17e793a1-26a3-4ecd-99ca-f38ecc6eaa2e`. - In progress: `20ce0cb1-387a-47d4-8c34-bc6fd3be0e27`. - Complete: `7223d809-553e-4714-a038-62dc98f3fbf3`. - Can't do: `06308884-41c2-4ee0-9da7-5676647d3d75`. |
| `modified_at` | body | `date` | no | Optional. The UTC time and date the modification took place. |
