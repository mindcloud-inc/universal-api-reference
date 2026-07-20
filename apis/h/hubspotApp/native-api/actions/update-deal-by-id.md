# Update Deal by ID with HubSpot

Updates an existing deal in HubSpot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v3/objects/deals/:dealId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Update Deal by ID](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/patch-crm-v3-objects-deals-dealId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dealId` | path | `string` | yes | HubSpot deal record ID to update. |
| `properties` | body | `object` | yes | Object of deal properties to update, for example {"dealstage":"appointmentscheduled"}. |
| `idProperty` | query | `string` | no | Unique property used to identify the deal instead of the internal record ID. |
