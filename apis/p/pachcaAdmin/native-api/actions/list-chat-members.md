# List Chat Members with Pachca (Admin)

Retrieves chat members from the Pachca Admin API.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:id/members`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Chat Members](https://dev.pachca.com/api/members/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca chat ID. |
| `role` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
