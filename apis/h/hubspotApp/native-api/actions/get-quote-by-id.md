# Get Quote by ID with HubSpot

Retrieves a quote from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/quotes/:quoteId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Quote by ID](https://developers.hubspot.com/docs/api-reference/crm-quotes-v3/basic/get-crm-v3-objects-quotes-quoteId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quoteId` | path | `string` | yes | HubSpot quote record ID. |
| `properties` | query | `string<string>` | no | Send multiple values as a string separated by `,`. |
