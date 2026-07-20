# Change User Display Name with Alpha TransForm

Updates a user's display name in Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/changeUserDisplayName/:userId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Change User Display Name](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeUserDisplayName.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | UserId |
| `userDisplayName` | query | `string` | no | New user display name |
