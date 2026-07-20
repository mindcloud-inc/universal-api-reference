# Update contact with Atera

Updates an existing contact in Atera.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/contacts/:contactId`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Update contact](https://app.atera.com/apidocs#!/Contact/Contact_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Archived` | body | `boolean` | no | Whether the contact is archived. |
| `contactId` | path | `number` | yes | System contact ID. |
| `CustomerID` | body | `number` | no | Customer ID. |
| `CustomerName` | body | `string` | no | Customer name. |
| `DepartmentID` | body | `number` | no | Department ID. |
| `DepartmentName` | body | `string` | no | Department name. |
| `Firstname` | body | `string` | no | Contact first name. |
| `InIgnoreMode` | body | `boolean` | no | Whether the contact is in ignore mode. |
| `IsContactPerson` | body | `boolean` | no | Whether this is the primary contact person. |
| `JobTitle` | body | `string` | no | Job title. |
| `Lastname` | body | `string` | no | Contact last name. |
| `MobilePhone` | body | `string` | no | Mobile phone number. |
| `Phone` | body | `string` | no | Phone number. |
