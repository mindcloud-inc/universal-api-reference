# List Customers with Retently

Retrieves a list of customers from Retently.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [List Customers](https://www.retently.com/api/#api-get-customers-get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Find a customer by the email address; |
| `page` | query | `number` | no | The current page number. Default 1; |
| `limit` | query | `number` | no | The items limit. Default 20. Maximum 1,000; |
| `sort` | query | `string` | no | The sort option. Use '-' for DESC. Default '-createdDate'; |
| `startDate` | query | `string` | no | ISO format or UNIX timestamp; |
| `endDate` | query | `string` | no | ISO format or UNIX timestamp; |
| `attributes[]` | query | `array<string>` | no | Filter by customer properties. See Attributes Filtering section below; |
| `match` | query | `string` | no | Logic for multiple attribute filters. Values: 'all' (AND, default), 'any' (OR); |
| `attributes[].name` | query | `string` | yes | Attribute field name |
| `attributes[].op` | query | `string` | yes | Filter operator |
| `attributes[].value` | query | `string` | yes | Attribute match value |
