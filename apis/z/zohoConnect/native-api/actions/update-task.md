# Update Task with Zoho Connect

Updates an existing task in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/updateTask`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Update Task](https://www.zoho.com/connect/api/update-task.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigneeId` | query | `string` | no | Comma-separated user IDs to assign to the task. Send multiple values as a string separated by `,`. |
| `desc` | query | `string` | no | Updated task description. |
| `edate` | query | `number` | no | Due date day. |
| `emonth` | query | `number` | no | Due date month. |
| `eyear` | query | `number` | no | Due date year. |
| `isClearDueDate` | query | `boolean` | no | Clear the task due date. |
| `priority` | query | `string` | yes | Priority level: None, Low, Medium, or High. |
| `removeAssigneeId` | query | `string` | no | Comma-separated user IDs to remove from the task. Send multiple values as a string separated by `,`. |
| `scopeID` | query | `string` | yes | ID of the network where the task exists. |
| `status` | query | `number` | no | Task status code: 0, 1, 2, 3, or 4. |
| `taskId` | query | `string` | yes | ID of the task to update. |
| `title` | query | `string` | yes | Updated task title. |
