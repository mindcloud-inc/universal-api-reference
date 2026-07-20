# Search Customers with Customer.io

Finds customers in Customer.io by filter.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Search Customers](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPeopleFilter)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | yes | A Customer.io audience filter object. |
