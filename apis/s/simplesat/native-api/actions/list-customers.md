# List Customers with Simplesat

Retrieves customers from Simplesat.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/customers`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [List Customers](https://developer.simplesat.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve |
| `page_size` | query | `number` | no | The number of records per page |
| `created_after` | query | `string` | no | Filter customers created after this date (ISO 8601 format) |
| `created_before` | query | `string` | no | Filter customers created before this date (ISO 8601 format) |
| `modified_after` | query | `string` | no | Filter customers modified after this date (ISO 8601 format) |
| `modified_before` | query | `string` | no | Filter customers modified before this date (ISO 8601 format) |
| `subscribed` | query | `boolean` | no | Filter customers by subscription status |
