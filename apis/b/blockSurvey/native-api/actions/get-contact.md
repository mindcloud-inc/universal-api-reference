# Get Contact with BlockSurvey

Retrieves a contact from BlockSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/get-contact`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Get Contact](https://documents.blocksurvey.io/audience/get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `string` | yes | ID of the team owning the list. |
| `listId` | body | `string` | yes | ID of the list containing the contact. |
| `listPrivateKey` | body | `string` | yes | Private key for decryption. |
| `recordId` | body | `string` | no | ID of the contact to retrieve. |
| `Email` | body | `string` | no | Email of the contact to retrieve. |
