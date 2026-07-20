# Update Contact with AvoSMS

Updates an existing contact in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/update`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Update Contact](https://www.avosms.com/en/api/documentation/contact/update)

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
