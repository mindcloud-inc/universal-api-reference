# Add Roles To Group with Frontegg

Adds roles to a user group in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/groups/v1/:groupId/roles`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Add Roles To Group](https://developers.frontegg.com/ciam/api/identity/user-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Group ID. |
| `roleIds[]` | body | `array<string>` | yes | Role IDs to add to the group. |
