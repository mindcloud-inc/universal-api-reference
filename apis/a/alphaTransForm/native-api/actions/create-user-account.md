# Create User Account with Alpha TransForm

Creates a new user account in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/createNewUserAccount`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Create User Account](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateNewUserAccount.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userid` | body | `string` | no | UserId |
| `password` | body | `string` | no | Password for the new user account |
| `roles` | body | `string` | no | Comma delimited list of roles for the new user in the account the user is added to |
| `displayname` | body | `string` | no | Display name for the user |
