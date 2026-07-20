# Create contact with Atera

Creates a contact in Atera.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/contacts`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Create contact](https://app.atera.com/apidocs#!/Contact/Contact_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CreatedOn` | body | `string` | no | Contact creation timestamp. |
| `CustomerID` | body | `number` | no | Existing customer ID. |
| `CustomerName` | body | `string` | no | Existing customer name. |
| `DepartmentID` | body | `number` | no | Department ID. |
| `DepartmentName` | body | `string` | no | Department name. |
| `Email` | body | `string` | yes | Contact email address. |
| `Firstname` | body | `string` | no | Contact first name. |
| `InIgnoreMode` | body | `boolean` | no | Whether the contact is in ignore mode. |
| `IsContactPerson` | body | `boolean` | no | Whether this is the primary contact person. |
| `JobTitle` | body | `string` | no | Job title. |
| `Lastname` | body | `string` | no | Contact last name. |
| `MobilePhone` | body | `string` | no | Mobile phone number. |
| `Phone` | body | `string` | no | Phone number. |
