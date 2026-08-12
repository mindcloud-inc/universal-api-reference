# Update Contact with Simpro

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:companyId/contacts/:contactId`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [Update Contact](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `contactId` | path | `number` | yes | Contact ID. |
| `GivenName` | body | `string` | no | Updated contact first name. |
| `Email` | body | `string` | no | Updated contact email. |
| `CellPhone` | body | `string` | no | Updated contact mobile phone. |
