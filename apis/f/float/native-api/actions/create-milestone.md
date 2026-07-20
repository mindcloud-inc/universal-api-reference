# Create Milestone with Float

Creates a new milestone in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/milestones`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Milestone](https://developer.float.com/api_reference.html#Milestones)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Start date of the milestone |
| `name` | body | `string` | yes | The name of the milestone |
| `phase_id` | body | `number` | no | The phase that this milestone belongs to |
| `project_id` | body | `number` | yes | The project that this milestone belongs to |
