# Create Assignment with Craftboxx

Creates an assignment in Craftboxx.

## Endpoint

- **Method:** `POST`
- **Path:** `assignments`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Create Assignment](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | body | `string` | no | The assignment end timestamp. |
| `start` | body | `string` | no | The assignment start timestamp. |
| `title` | body | `string` | yes | The assignment title. |
| `project_id` | body | `number` | yes | The project ID for the assignment. |
