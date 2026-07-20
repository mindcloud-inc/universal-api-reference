# List Deal Quotes with HubSpot

Retrieves quotes associated with a HubSpot deal.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/deals/:dealId/associations/quotes`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Deal Quotes](https://developers.hubspot.com/docs/api-reference/crm-associations-v3/guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dealId` | path | `string` | yes | HubSpot deal record ID. |
