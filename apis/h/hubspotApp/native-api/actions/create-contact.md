# Create Contact with HubSpot

Creates a new contact in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/contacts`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Contact](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/post-crm-v3-objects-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `associations[].to` | body | `object` | no | — |
| `associations[].to.id` | body | `string` | no | Id of the object to associate |
| `associations[].types[].associationCategory` | body | `list<string>` | no | This represents if the association you're creating is default created by HupSpot, or it is a custom association the user defined. |
| `properties` | body | `object` | yes | — |
| `associations[]` | body | `array<object>` | no | — |
| `associations[].types[]` | body | `array` | no | — |
| `associations[].types[].associationTypeId` | body | `string` | no | Check for types at: https://developers.hubspot.com/docs/api-reference/crm-associations-v4/guide#association-type-id-values |
| `properties.firstname` | body | `string` | no | — |
| `properties.lastname` | body | `string` | no | — |
| `properties.email` | body | `string` | no | — |
| `properties.mobilephone` | body | `string` | no | — |
| `properties.phone` | body | `string` | no | — |
| `properties.jobtitle` | body | `string` | no | — |
