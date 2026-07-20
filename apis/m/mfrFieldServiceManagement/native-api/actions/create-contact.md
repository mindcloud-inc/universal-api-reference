# Create Contact with mfr Field Service Management

Creates a contact in mfr Field Service Management.

## Endpoint

- **Method:** `POST`
- **Path:** `Contacts`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Create Contact](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FirstName` | body | `string` | yes | Contact first name. |
| `LastName` | body | `string` | yes | Contact last name. |
| `Email` | body | `string` | no | Contact email address. |
| `CompanyId` | body | `string` | no | Company ID linked to the contact. |
| `ExternalId` | body | `string` | no | External identifier for the contact. |
| `MobilePhone` | body | `string` | no | Contact mobile phone number. |
| `Telephone` | body | `string` | no | Contact telephone number. |
| `IsUser` | body | `boolean` | no | Whether the contact is a user. |
| `Gender` | body | `string` | no | Contact gender. |
| `Fax` | body | `string` | no | Contact fax number. |
| `Note` | body | `string` | no | Contact note. |
| `JobTitle` | body | `string` | no | Contact job title. |
