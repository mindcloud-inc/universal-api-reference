# Update Column with FlowFast

Updates an existing column in FlowFast.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/boards/:boardId/columns/:columnId`
- **Base URL:** `https://apps.flowfast.io/api/latest/`
- **Official documentation:** [Update Column](https://apps.flowfast.io)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardId` | path | `string` | no |
| `columnId` | path | `string` | no |
| `title` | body | `string` | no |
