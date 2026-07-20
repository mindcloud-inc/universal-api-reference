# List Deal Line Items with HubSpot

Retrieves line items associated with a HubSpot deal.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/deals/:dealId/associations/line_items`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Deal Line Items](https://developers.hubspot.com/docs/api-reference/crm-associations-v3/guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dealId` | path | `string` | yes | The unique ID of the deal whose line item associations to retrieve. |
