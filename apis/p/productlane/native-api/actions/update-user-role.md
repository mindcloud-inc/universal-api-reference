# Update User Role with Productlane

Updates a user's role in Productlane.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/role`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update User Role](https://productlane.mintlify.dev/docs/api/users/update-user-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `membershipId` | body | `string` | yes | Workspace membership ID to change. |
| `role` | body | `string` | yes | New role for the membership. |
