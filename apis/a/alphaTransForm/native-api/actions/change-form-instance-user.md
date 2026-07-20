# Change Form Instance User with Alpha TransForm

Updates the user for a form instance in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/ChangeFormInstanceUserId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Change Form Instance User](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceUserId.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formInstanceId` | body | `string` | no | useridCharacter The user id (i.e. email) of the user to whom the form instance should be assigned |
