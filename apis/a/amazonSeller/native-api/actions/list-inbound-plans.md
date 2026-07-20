# List Inbound Plans with Amazon Seller

Retrieves inbound plans from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `inbound/fba/2024-03-20/inboundPlans`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** pageSize / paginationToken
- **Official documentation:** [List Inbound Plans](https://developer-docs.amazon.com/sp-api/reference/listinboundplans)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | The status of an inbound plan. |
