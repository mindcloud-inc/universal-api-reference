# Create Contact with BlockSurvey

Creates a new contact in BlockSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/create-contact`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Create Contact](https://documents.blocksurvey.io/audience/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `string` | yes | ID of the team owning the list. |
| `listId` | body | `string` | yes | ID of the list to add the contact. |
| `listPublicKey` | body | `string` | yes | Public key for encryption. |
| `Email` | body | `string` | yes | Email address of the contact. |
| `First Name` | body | `string` | no | First name of the contact. |
| `Last Name` | body | `string` | no | Last name of the contact. |
| `Phone Number` | body | `string` | no | Phone number of the contact. |
| `Country` | body | `string` | no | Country of the contact. |
