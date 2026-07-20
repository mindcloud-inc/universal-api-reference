# List Sales Orders with Fiddle

Retrieves sales order records from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales-orders`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Sales Orders](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | query | `string` | no | Customer ID filter |
| `status` | query | `string` | no | Status filter |
