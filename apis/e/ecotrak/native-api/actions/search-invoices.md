# Search Invoices with Ecotrak

Finds invoices in Ecotrak by approved or created date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/invoices/search`
- **Base URL:** `https://api.ecotrak.com`
- **Official documentation:** [Search Invoices](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-invoices-search-invoices)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approved_date` | query | `string` | no | The date for which approved invoices are to be searched. Format YYYY-MM-DD. |
| `exclude_location_type_id` | query | `number` | no | The ID of the location type to be excluded from the search. |
| `created_at` | query | `string` | no | The date for which invoices were created. Format YYYY-MM-DD. |
