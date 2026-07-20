# List Customers with ChartMogul

Retrieves customers from ChartMogul.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.chartmogul.com/v1`
- **Official documentation:** [List Customers](https://dev.chartmogul.com/reference/customers/list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_source_uuid` | query | `string` | no | Filter customers by data source UUID. |
| `email` | query | `string` | no | Search for customers by email address. |
| `external_id` | query | `string` | no | Filter by the customer external identifier. |
| `status` | query | `string` | no | Filter by customer status. |
| `system` | query | `string` | no | Filter by billing system type. |
| `with_associated_emails` | query | `boolean` | no | Include customers linked through associated contact email addresses. |
