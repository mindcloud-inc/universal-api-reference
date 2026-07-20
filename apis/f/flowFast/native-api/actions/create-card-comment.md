# Create Card Comment with FlowFast

Creates a new comment on a card in FlowFast.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards/:cardId/comments`
- **Base URL:** `https://apps.flowfast.io/api/latest/`
- **Official documentation:** [Create Card Comment](https://apps.flowfast.io)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cardId` | path | `string` | no |
| `text` | body | `string` | no |
