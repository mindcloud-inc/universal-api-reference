# Update Contact with mfr Field Service Management

Updates a contact in mfr Field Service Management.

## Endpoint

- **Method:** `PUT`
- **Path:** `Contacts({{id}}L)`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Update Contact](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `FirstName` | body | `string` | no | Updated contact first name. |
| `Id` | body | `string` | yes | Record ID in the request body. |
| `LastName` | body | `string` | no | Updated contact last name. |
| `Email` | body | `string` | no | Updated contact email address. |
| `JobTitle` | body | `string` | no | Updated job title. |
| `ExternalId` | body | `string` | no | Updated external identifier. |
| `MobilePhone` | body | `string` | no | Mobile phone number. |
| `Telephone` | body | `string` | no | Telephone number. |
| `Fax` | body | `string` | no | Fax number. |
| `Note` | body | `string` | no | Contact note. |
| `CompanyId` | body | `string` | no | Associated company identifier. |
| `IsUser` | body | `boolean` | no | Whether the contact is a user. |
| `Gender` | body | `string` | no | Contact gender. |
