# Remove Reaction with Pachca (Admin)

Deletes a reaction from the Pachca Admin API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messages/:id/reactions`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Remove Reaction](https://dev.pachca.com/api/reactions/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca message ID. |
| `code` | query | `string` | yes | — |
| `name` | query | `string` | no | — |
