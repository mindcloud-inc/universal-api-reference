# Delete Contact with BlockSurvey

Deletes a contact from BlockSurvey.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact/delete-contact`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Delete Contact](https://documents.blocksurvey.io/audience/delete-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `string` | yes | ID of the team owning the list. |
| `listId` | body | `string` | yes | ID of the list containing the contact. |
| `recordId` | body | `string` | no | ID of the contact to delete. |
| `Email` | body | `string` | no | Email of the contact to delete. |
