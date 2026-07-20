# Create Workflow with Port API AI

Creates a workflow in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Workflow](https://docs.port.io/api-reference/create-a-workflow)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | body | `string` | yes |
| `title` | body | `string` | no |
| `icon` | body | `string` | no |
| `nodes[]` | body | `array<object>` | yes |
| `connections[]` | body | `array<object>` | no |
