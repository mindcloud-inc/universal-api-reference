# Update Company by ID with HubSpot

Updates an existing company in HubSpot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v3/objects/companies/:companyId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Update Company by ID](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/patch-crm-v3-objects-companies-companyId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | HubSpot company record ID to update. |
| `properties` | body | `object` | yes | Object of company properties to update, e.g. {"arr":"250000"}. |
| `idProperty` | query | `string` | no | Unique property used to identify record instead of internal ID. |
