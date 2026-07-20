# List Invoices with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [List Invoices](https://docs.housecallpro.com/docs/housecall-public-api/65ce9f430d605)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_ids[]` | query | `array<string>` | no | Filter invoices by location ids. Send multiple values as a array. |
| `status` | query | `list<string>` | no | Filter invoices by status. Accepted values: `canceled`, `open`, `paid`, `pending_payment`, `uncollectible`, `voided`. Send multiple values as a array. |
| `customer_uuid[]` | query | `array<string>` | no | Filter invoices by customer UUIDs. Send multiple values as a array. |
| `created_at_min` | query | `date` | no | Filter invoices created on or after this timestamp. |
| `created_at_max` | query | `date` | no | Filter invoices created on or before this timestamp. |
| `due_at_min` | query | `date` | no | Filter invoices due on or after this timestamp. |
| `due_at_max` | query | `date` | no | Filter invoices due on or before this timestamp. |
| `paid_at_min` | query | `date` | no | Filter invoices paid on or after this timestamp. |
| `paid_at_max` | query | `date` | no | Filter invoices paid on or before this timestamp. |
| `amount_due_min` | query | `number` | no | Filter invoices with due amount at or above this value. |
| `amount_due_max` | query | `number` | no | Filter invoices with due amount at or below this value. |
| `payment_method` | query | `list<string>` | no | Filter invoices by payment method. Accepted values: `ach`, `consumer_financing`, `credit_card`, `external`, `mobile_check_deposit`. Send multiple values as a array. |
