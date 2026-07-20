# Update Task with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Update Task](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-EditTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TaskId` | body | `string` | yes | The task Id to update. |
| `Name` | body | `string` | no | Updated task name. |
| `DueDate` | body | `date` | no | Updated due date. |
| `AssignedTo` | body | `string` | no | Updated assignee user Id. |
| `CalendarId` | body | `string` | no | Updated calendar Id. |
| `Description` | body | `string` | no | Updated task details. |
| `ContactId` | body | `string` | no | Updated attached contact or company Id, or null to detach. |
| `IsComplete` | body | `boolean` | no | Mark the task complete or incomplete. |
