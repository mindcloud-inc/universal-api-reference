# Set User Roles In Account with Alpha TransForm

Updates a user's account roles in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/setUserRolesInAccount/:userId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Set User Roles In Account](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/SetUserRolesInAccount.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | UserId |
| `roles` | body | `string` | no | Comma delimited list of roles |
