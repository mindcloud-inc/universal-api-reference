# Add User To Account with Alpha TransForm

Adds a user to an Alpha TransForm account.

## Endpoint

- **Method:** `GET`
- **Path:** `/addUserToTransFormAccount/`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Add User To Account](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/AddUserToTransFormAccount.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | no | UserId to add to TransForm account |
| `roles` | query | `string` | no | Roles for user in this TransForm account |
| `validateUser` | query | `boolean` | no | If true only people with valid TransForm user accounts are added |
