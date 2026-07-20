# Delete User Roles In Account with Alpha TransForm

Deletes a user's account roles from Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/deleteUserRolesInAccount/:userIdToDelete`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Delete User Roles In Account](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/DeleteUserRolesInAccount.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | no | UserId |
| `userIdToDelete` | path | `string` | yes | — |
| `roles` | query | `string` | no | Comma delimited list of roles |
