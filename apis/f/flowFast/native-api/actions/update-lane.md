# Update Lane with FlowFast

Updates an existing lane in FlowFast.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/boards/:boardId/lanes/:laneId`
- **Base URL:** `https://apps.flowfast.io/api/latest/`
- **Official documentation:** [Update Lane](https://apps.flowfast.io)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardId` | path | `string` | no |
| `laneId` | path | `string` | no |
| `title` | body | `string` | no |
