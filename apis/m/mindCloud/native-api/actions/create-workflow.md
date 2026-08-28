# Create Workflow with MindCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/workflows`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Create Workflow](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for this MindCloud v2 request. |
| `tags[]` | body | `array<string>` | no | Tags for this MindCloud v2 request. |
