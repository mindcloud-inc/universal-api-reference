# Edit Contact with Formitize

Updates an existing contact in Formitize.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/client/:id/contact/:contactID`
- **Base URL:** `https://service.formitize.com/api/rest/v2`
- **Official documentation:** [Edit Contact](https://mitechnologies.github.io/Formitize-NET-API/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactID` | path | `string` | no | Formitize contact ID. |
| `id` | path | `string` | no | Formitize client ID for contact update path. |
