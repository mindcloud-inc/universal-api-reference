# List Workflow History with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/history`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [List Workflow History](https://api.gocanvas.com/api/v3/docs#workflow-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | AssignedToMe, AssignedToSomeoneElse, or Completed; any other value is treated as a submission client GUID. Omit for full history. |
