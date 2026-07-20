# Update Contact with BlockSurvey

Updates an existing contact in BlockSurvey.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/update-contact`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Update Contact](https://documents.blocksurvey.io/audience/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `string` | yes | ID of the team owning the list. |
| `listId` | body | `string` | yes | ID of the list containing the contact. |
| `listPublicKey` | body | `string` | yes | Public key for encryption. |
| `recordId` | body | `string` | no | ID of the contact to update. |
| `oldEmail` | body | `string` | no | Old email of the contact. |
| `Email` | body | `string` | no | New email of the contact. |
| `First Name` | body | `string` | no | First name of the contact. |
| `Last Name` | body | `string` | no | Last name of the contact. |
| `Phone Number` | body | `string` | no | Phone number of the contact. |
| `Country` | body | `string` | no | Country of the contact. |
