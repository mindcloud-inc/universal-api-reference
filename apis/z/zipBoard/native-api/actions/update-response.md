# Update Response with zipBoard

Updates an existing response in zipBoard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/issues/responses/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Update Response](https://docs.zipboard.co/#tag/Responses/paths/~1api~1v1~1issues~1responses~1{id}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `mentionedIds[]` | body | `array<string>` | no |
| `reply` | body | `string` | yes |
