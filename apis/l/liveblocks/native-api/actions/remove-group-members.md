# Remove Group Members with Liveblocks

Updates a Liveblocks group by removing members.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/remove-members`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Remove Group Members](https://liveblocks.io/docs/api-reference/rest-api-endpoints#remove-group-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | no | ID of the group. |
| `memberIds[]` | body | `array<string>` | no | — |
