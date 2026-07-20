# Create Task with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Create Task](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-CreateTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Task name shown on the task list. |
| `DueDate` | body | `date` | no | Date the task should appear. |
| `AssignedTo` | body | `string` | no | User Id the task should be assigned to. |
| `CalendarId` | body | `string` | no | Calendar Id to categorize the task under. |
| `Description` | body | `string` | no | Additional task details. |
| `ContactId` | body | `string` | no | Optional contact or company Id to attach the task to. |
