# Update Invoice by ID with HubSpot

Updates an existing invoice in HubSpot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v3/objects/invoices/:invoiceId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Update Invoice by ID](https://developers.hubspot.com/docs/api-reference/crm-invoices-v3/basic/patch-crm-v3-objects-invoices-invoiceId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceId` | path | `string` | yes | — |
| `properties` | body | `object` | yes | The invoice property values to update. |
| `idProperty` | query | `string` | no | The property to use instead of the record ID when identifying the invoice. |
