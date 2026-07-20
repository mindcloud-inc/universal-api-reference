# List Partner Customers with Escrow.com

Retrieves partner customers from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/partner/customers`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [List Partner Customers](https://www.escrow.com/api/docs/reference)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum partner customers to fetch. |
| `next_cursor` | query | `number` | no | Cursor to start fetching partner customers from. |
| `sort_by` | query | `string` | no | Partner customer sort field. Escrow.com documents id as a valid value. |
| `sort_direction` | query | `string` | no | Sort direction, asc or desc. |
| `country` | query | `string` | no | Filter customers by country code, such as AU or US. |
| `verification_status` | query | `string` | no | Filter customers by verification status: verified, not_verified, or company_verified. |
| `ids[]` | query | `array<number>` | no | Customer IDs to filter by. |
