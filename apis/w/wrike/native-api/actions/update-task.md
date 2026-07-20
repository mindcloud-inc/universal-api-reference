# Update Task with Wrike

Updates an existing task in Wrike.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Update Task](https://developers.wrike.com/api/v4/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Wrike task ID. |
| `title` | query | `string` | no | Title of task |
| `description` | query | `string` | no | Task description |
| `status` | query | `list` | no | Task status Accepted values: `Active`, `Cancelled`, `Completed`, `Deferred`. |
| `importance` | query | `list` | no | Task importance Accepted values: `High`, `Low`, `Normal`. |
| `dates` | query | `string` | no | Task dates as a JSON object string |
| `addParents` | query | `string` | no | Folder IDs to add as parents, as a JSON string array |
| `removeParents` | query | `string` | no | Folder IDs to remove as parents, as a JSON string array |
| `addShareds` | query | `string` | no | User or invitation IDs to share with, as a JSON string array |
| `removeShareds` | query | `string` | no | User or invitation IDs to unshare, as a JSON string array |
| `addResponsibles` | query | `string` | no | User or invitation IDs to add as assignees, as a JSON string array |
| `removeResponsibles` | query | `string` | no | User or invitation IDs to remove as assignees, as a JSON string array |
| `addResponsiblePlaceholders` | query | `string` | no | Placeholder IDs to add as assignees, as a JSON string array |
| `removeResponsiblePlaceholders` | query | `string` | no | Placeholder IDs to remove as assignees, as a JSON string array |
| `addFollowers` | query | `string` | no | User IDs to add as followers, as a JSON string array |
| `follow` | query | `boolean` | no | Follow task |
| `priorityBefore` | query | `string` | no | Put task before this task ID |
| `priorityAfter` | query | `string` | no | Put task after this task ID |
| `addSuperTasks` | query | `string` | no | Parent task IDs to add, as a JSON string array |
| `removeSuperTasks` | query | `string` | no | Parent task IDs to remove, as a JSON string array |
| `metadata` | query | `string` | no | Metadata entries to update, as a JSON string array |
| `customFields` | query | `string` | no | Custom field values to update, as a JSON string array |
| `customStatus` | query | `string` | no | Custom status ID |
| `restore` | query | `boolean` | no | Restore task from recycled bin |
| `effortAllocation` | query | `string` | no | Effort allocation as a JSON object string |
| `setResponsibleAllocation` | query | `string` | no | Responsible allocations as a JSON string array |
| `billingType` | query | `list` | no | Task timelog billing type Accepted values: `Billable`, `NonBillable`. |
| `withInvitations` | query | `boolean` | no | Include invitations in shared and responsible lists |
| `convertToCustomItemType` | query | `string` | no | Custom item type ID |
| `plainTextCustomFields` | query | `boolean` | no | Strip HTML tags from custom fields |
| `workScheduleId` | query | `string` | no | Work schedule ID to assign to the task |
| `fields` | query | `string` | no | Response field names as a JSON string array |
