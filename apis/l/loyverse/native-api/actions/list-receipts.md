# List Receipts with Loyverse

Retrieves sales receipt records from Loyverse.

## Endpoint

- **Method:** `GET`
- **Path:** `/receipts`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Receipts](https://developer.loyverse.com/docs/#tag/Receipts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receipt_numbers` | query | `string` | no | Return only receipts specified by a comma-separated list of receipt numbers |
| `since_receipt_number` | query | `string` | no | Show receipts since date which is equal to created_at date of the receipt with specified number |
| `before_receipt_number` | query | `string` | no | Show receipts up to date which is equal to created_at date of the receipt with specified number |
| `store_id` | query | `string` | no | Show receipts only for specified store |
| `order` | query | `string` | no | Filter receipts by order |
| `source` | query | `string` | no | The name of the the source this receipt comes from |
| `updated_at_min` | query | `date` | no | Show receipts updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_max` | query | `date` | no | Show receipts updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `created_at_min` | query | `date` | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `created_at_max` | query | `date` | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |
