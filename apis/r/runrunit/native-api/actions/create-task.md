# Create Task with Runrun.it

Creates a new task in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Create Task](https://runrun.it/api/documentation#tasks-create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task.title` | body | `string` | yes | Task title |
| `task.on_going` | body | `boolean` | no | True if the task is an ongoing task |
| `task.type_id` | body | `number` | yes | ID of the task type |
| `task.project_id` | body | `number` | no | ID of the project the task belongs to |
| `task.desired_start_date` | body | `date` | no | Desired start date |
| `task.desired_date` | body | `date` | no | Desired delivery date |
| `task.tag_list` | body | `string` | no | Task tag list |
| `task.assignments[]` | body | `array<object>` | no | Objects of task assignments |
| `task.task_prerequisite_ids[]` | body | `array<string>` | no | IDs of pre-requisite tasks |
| `task.task_descendant_ids[]` | body | `array<string>` | no | IDs of descendant tasks |
| `task.follower_ids[]` | body | `array<string>` | no | IDs of users to follow this task |
| `task.document_ids[]` | body | `array<string>` | no | IDs of Document records to attach |
