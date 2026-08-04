# Create Company with HubSpot

Creates a new company in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/companies`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Company](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/post-crm-v3-objects-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `associations[].to` | body | `object` | no | — |
| `associations[].to.id` | body | `string` | no | Id of the object to associate |
| `associations[].types[].associationCategory` | body | `list` | no | This represents if the association you're creating is default created by HupSpot, or it is a custom association the user defined. |
| `properties` | body | `object` | no | — |
| `properties.name` | body | `string` | no | — |
| `associations[]` | body | `array<object>` | no | — |
| `associations[].types[]` | body | `array<object>` | no | — |
| `associations[].types[].associationTypeId` | body | `string` | no | Check for types at: https://developers.hubspot.com/docs/api-reference/crm-associations-v4/guide#association-type-id-values |
| `properties.domain` | body | `string` | no | — |
| `properties.city` | body | `string` | no | — |
| `properties.industry` | body | `string` | no | — |
| `properties.phone` | body | `string` | no | — |
| `properties.state` | body | `string` | no | — |
| `properties.lifecycleStage` | body | `string` | no | — |
| `properties.address` | body | `string` | no | — |
| `properties.acumatica_customer_id` | body | `string` | no | — |
| `properties.acumatica_location_id` | body | `string` | no | — |
