# Add Chat Members with Pachca (Admin)

Adds chat members in the Pachca Admin API.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/:id/members`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Add Chat Members](https://dev.pachca.com/api/members/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca chat ID. |
| `member_ids[]` | body | `array<number>` | yes | — |
| `silent` | body | `boolean` | no | — |
