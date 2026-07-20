# Add Users To Group with Frontegg

Adds users to a user group in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/groups/v1/:groupId/users`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Add Users To Group](https://developers.frontegg.com/ciam/api/identity/user-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Group ID. |
| `userIds[]` | body | `array<string>` | yes | User IDs to add to the group. |
