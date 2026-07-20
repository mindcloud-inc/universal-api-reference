# List Reactions with Pachca (Admin)

Retrieves reactions from the Pachca Admin API.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:id/reactions`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Reactions](https://dev.pachca.com/api/reactions/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca message ID. |
| `limit` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
