# Create Task with Rocketlane

Creates a task in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/tasks`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Create Task](https://developer.rocketlane.com/reference/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `taskId` | body | `number` | no | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `taskName` | body | `string` | yes | The **name** of the task. |
| `taskDescription` | body | `string` | no | The `description` of the task. The description body needs to be in **html** format to avoid any formatting issues in the application. |
| `taskPrivateNote` | body | `string` | no | The `privateNote` for the task is intended exclusively for team members. The note's content should be in `HTML` format to prevent any formatting issues in the application. |
| `startDate` | body | `string` | no | The date when a task starts its execution. It can be empty. The format for the start date is _YYYY-MM-DD_. |
| `dueDate` | body | `string` | no | The date when a task completes its execution. It can be empty. If both `startDate` and `dueDate` are specified for a given task, it is necessary that the latter should be on or after the given `startDate`. The format for the due date is _YYYY-MM-DD_. |
| `effortInMinutes` | body | `number` | no | The effort is the expected time required to complete the task. The value is determined in minutes. |
| `progress` | body | `number` | no | The task's progress, if indicated, will be available here and ranges in value from 0 to 100. The task's status can be used in place of this field, however progress can offer more precise data. |
| `atRisk` | body | `boolean` | no | Indicates whether the task has been marked as At Risk. This parameter is used to indicate that immediate action is necessary to unblock the task's execution. |
| `type` | body | `string` | no | The type of the task if specified will be available here. There are two options: `MILESTONE` or `TASK`. If a task is not explicitly marked as a milestone, it takes the default value as `TASK`. Milestones refer to critical tasks in the project that include an inbuilt CSAT capability that allows customers to offer CSAT evaluations depending on the task's execution. |
| `project` | body | `object` | yes | The `project` associated with task needs to be specified here and it is mandatory for the task to get created and map accordingly. |
| `phase` | body | `object` | no | The `phase` that needs to be associated with the task can be mentioned here. Note: The `phase` needs to be associated with the `project` and thus failing the task creation process. |
| `status` | body | `object` | no | The value of the task status can be specified here and this is essential to keep track of it. |
| `fields` | body | `list<object>` | no | The custom fields can be set during the task creation with the help of `fields`. The `fieldValue` can be either a string or a number or an array and it has to comply with the type of the field. Refer [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know how to assign `fieldValue` based on their `field_type`. |
| `assignees` | body | `object` | no | — |
| `followers` | body | `object` | no | The task followers can be either `members` (team members or customers) or `placeholders`. |
| `parent` | body | `object` | no | Parent task id |
| `externalReferenceId` | body | `string` | no | An externalReferenceId is a unique identifier that links entities or transactions between external systems and Rocketlane, ensuring accurate data correlation and consistency. |
| `source` | body | `object` | no | Source information for importing a task from a template |
| `private` | body | `boolean` | no | This depicts if the task is private or not. |
