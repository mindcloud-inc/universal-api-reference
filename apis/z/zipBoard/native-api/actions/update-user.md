# Update User with zipBoard

Updates an existing user in zipBoard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Update User](https://docs.zipboard.co/#tag/Users/paths/~1api~1v1~1user~1{id}/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `isExtensionOnboarded` | body | `string` | yes |
