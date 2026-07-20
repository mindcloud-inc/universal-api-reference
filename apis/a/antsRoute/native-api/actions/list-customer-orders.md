# List Customer Orders with AntsRoute

Finds orders in AntsRoute for a customer.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/customer/id/:id/orders`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [List Customer Orders](https://app.antsroute.com/doc-api/index.html#/Customer/getCustomerOrdersById)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `maxDate` | query | `date` | no | Filter by schedule date less than this date |
| `minDate` | query | `date` | no | Filter by schedule date greater than this date |
| `states[]` | query | `array<string>` | no | Filter by states |
