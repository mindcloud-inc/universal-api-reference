# Delete Contact with Formitize

Deletes an existing contact from Formitize.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/crm/client/:id/contact/:contactID`
- **Base URL:** `https://service.formitize.com/api/rest/v2`
- **Official documentation:** [Delete Contact](https://mitechnologies.github.io/Formitize-NET-API/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactID` | path | `string` | no | Formitize contact ID. |
| `id` | path | `string` | no | Formitize client ID for contact delete path. |
