# Create Task with Wrike

Creates a new task in a Wrike folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:folderId/tasks`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Create Task](https://developers.wrike.com/api/v4/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Wrike folder ID where the task will be created. |
| `title` | query | `string` | yes | Title of task, required |
| `description` | query | `string` | no | Description of task, will be left blank if not set |
| `status` | query | `list` | no | Task status Accepted values: `Active`, `Cancelled`, `Completed`, `Deferred`. |
| `importance` | query | `list` | no | Task importance Accepted values: `High`, `Low`, `Normal`. |
| `dates` | query | `string` | no | Task dates as a JSON object string |
| `shareds` | query | `string` | no | User or invitation IDs as a JSON string array |
| `parents` | query | `string` | no | Parent folder IDs as a JSON string array |
| `responsibles` | query | `string` | no | Assignee user or invitation IDs as a JSON string array |
| `responsiblePlaceholders` | query | `string` | no | Placeholder assignee IDs as a JSON string array |
| `followers` | query | `string` | no | Follower user IDs as a JSON string array |
| `follow` | query | `boolean` | no | Follow task |
| `priorityBefore` | query | `string` | no | Put newly created task before this task ID |
| `priorityAfter` | query | `string` | no | Put newly created task after this task ID |
| `superTasks` | query | `string` | no | Parent task IDs as a JSON string array |
| `metadata` | query | `string` | no | Metadata entries as a JSON string array |
| `customFields` | query | `string` | no | Custom field values as a JSON string array |
| `customStatus` | query | `string` | no | Custom status ID |
| `effortAllocation` | query | `string` | no | Effort allocation as a JSON object string |
| `billingType` | query | `list` | no | Task timelog billing type Accepted values: `Billable`, `NonBillable`. |
| `withInvitations` | query | `boolean` | no | Include invitations in shared and responsible lists |
| `customItemTypeId` | query | `string` | no | Custom item type ID to create a task from |
| `plainTextCustomFields` | query | `boolean` | no | Strip HTML tags from custom fields |
| `workScheduleId` | query | `string` | no | Work schedule ID to assign to the task |
| `fields` | query | `string` | no | Response field names as a JSON string array |
