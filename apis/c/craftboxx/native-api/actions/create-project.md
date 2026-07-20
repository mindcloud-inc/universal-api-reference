# Create Project with Craftboxx

Creates a project in Craftboxx.

## Endpoint

- **Method:** `POST`
- **Path:** `projects`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Create Project](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The project title. |
| `customer_id` | body | `number` | yes | The customer ID for the project. |
