# Add Contact with AvoSMS

Creates a new contact in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/add`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Add Contact](https://www.avosms.com/en/api/documentation/contact/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listContactId` | body | `string` | yes | Contact list ID |
| `contactTelephoneNumber` | body | `string` | yes | Contact phone number |
| `contactCivility` | body | `string` | no | Civility of the contact |
| `contactName` | body | `string` | no | Contact last name |
| `contactFirstName` | body | `string` | no | Contact first name |
| `contactEmail` | body | `string` | no | Contact email address |
| `contactBirthday` | body | `string` | no | Contact birthday |
| `contactOther` | body | `string` | no | Other contact information |
