# List Customers with AntsRoute

Finds customer records in your AntsRoute site.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/customer`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [List Customers](https://app.antsroute.com/doc-api/index.html#/Customer/findAllCustomers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeSectors` | query | `boolean` | no | Return sectors assigned to this customer |
