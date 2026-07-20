# Create Workspace with SectorFlow.AI

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Create Workspace](https://docs.sectorflowai.com/reference/getting-started-with-your-api-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Workspace name. |
| `modelIds[]` | body | `array<string>` | yes | List of model UUIDs. |
