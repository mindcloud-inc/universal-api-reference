# Delete Form User with Global Patron

Deletes a form user from Global Patron.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/restricted/form/{formId}/usersecurity/{userSecurityDocumentId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Delete Form User](https://www.globalpatron.com/developers/api/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `userSecurityDocumentId` | path | `string` | yes | ID of the user security document to delete. |
