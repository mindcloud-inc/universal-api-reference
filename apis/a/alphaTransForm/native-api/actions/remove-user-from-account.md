# Remove User From Account with Alpha TransForm

Removes a user from an Alpha TransForm account.

## Endpoint

- **Method:** `POST`
- **Path:** `/removeUserFromTransFormAccount/:accountToRemoveFrom`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Remove User From Account](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/RemoveUserFromTransFormAccount.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdToRemove` | body | `string` | no | UserId to remove from TransForm account |
| `accountToRemoveFrom` | path | `string` | yes | Only super users can specify an accountId. Otherwise TransForm account associated with API key is used. |
