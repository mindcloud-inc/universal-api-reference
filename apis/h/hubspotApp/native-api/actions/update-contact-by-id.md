# Update Contact by ID with HubSpot

Updates an existing contact in HubSpot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v3/objects/contacts/:contactId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Update Contact by ID](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/patch-crm-v3-objects-contacts-contactId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Contact ID to update. |
| `properties.firstname` | body | `string` | no | — |
| `properties` | body | `object` | yes | Properties object to update. |
| `properties.lastname` | body | `string` | no | — |
