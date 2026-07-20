# Create Phase with Float

Creates a new phase in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/phases`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Phase](https://developer.float.com/api_reference.html#Phases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | body | `string` | yes | The end date of this phase |
| `name` | body | `string` | yes | The name of the phase |
| `project_id` | body | `number` | yes | The ID of the project to which this phase belongs |
| `start_date` | body | `string` | yes | The start date of this phase |
