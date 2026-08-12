# Create Contact with Simpro

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/contacts/`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [Create Contact](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `GivenName` | body | `string` | yes | Contact first name. |
| `FamilyName` | body | `string` | no | Contact last name. |
| `Email` | body | `string` | no | Contact email address. |
| `CellPhone` | body | `string` | no | Contact mobile phone. |
