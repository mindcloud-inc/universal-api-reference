# Create Allocation with Float

Creates a new allocation in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Allocation](https://developer.float.com/api_reference.html#Allocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | The ID of the project for this allocation |
| `phase_id` | body | `number` | no | The ID of the project phase for this allocation |
| `start_date` | body | `string` | yes | Start date of this allocation |
| `end_date` | body | `string` | yes | End date of this allocation |
| `start_time` | body | `string` | no | Start time in 24 hour format |
| `hours` | body | `number` | yes | Number of hours per day |
| `people_id` | body | `number` | no | The ID of the person assigned to the allocation |
| `people_ids` | body | `list<number>` | no | List of one or more people IDs assigned to the allocation |
| `status` | body | `number` | no | Status of the allocation |
| `name` | body | `string` | no | Name of the associated project task |
| `task_meta_id` | body | `number` | no | The ID of the associated project task |
| `notes` | body | `string` | no | Additional details about the work required |
| `repeat_state` | body | `number` | no | Frequency that this allocation repeats |
| `repeat_end_date` | body | `string` | no | Date that the repeating allocation will cease |
