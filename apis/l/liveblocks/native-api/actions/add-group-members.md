# Add Group Members with Liveblocks

Updates a Liveblocks group by adding members.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/add-members`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Add Group Members](https://liveblocks.io/docs/api-reference/rest-api-endpoints#add-group-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | no | ID of the group. |
| `memberIds[]` | body | `array<string>` | no | — |
