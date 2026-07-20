# Update Card Comment with FlowFast

Updates an existing card comment in FlowFast.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/cards/:cardId/comments/:commentId`
- **Base URL:** `https://apps.flowfast.io/api/latest/`
- **Official documentation:** [Update Card Comment](https://apps.flowfast.io)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cardId` | path | `string` | no |
| `commentId` | path | `string` | no |
| `text` | body | `string` | no |
