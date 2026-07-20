# Create Expense with Bexio

Creates an expense in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/4.0/expenses`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Create Expense](https://docs.bexio.com/#tag/Expenses/operation/ApiExpenses_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paid_on` | body | `date` | yes | Date when the expense was paid. |
| `currency_code` | body | `string` | yes | — |
| `supplier_id` | body | `number` | no | — |
| `title` | body | `string` | no | — |
| `bank_account_id` | body | `number` | no | — |
| `booking_account_id` | body | `number` | no | — |
| `amount` | body | `number` | yes | — |
| `tax_id` | body | `number` | no | — |
| `exchange_rate` | body | `number` | no | — |
| `base_currency_amount` | body | `number` | no | — |
| `attachment_ids[]` | body | `array<string>` | yes | — |
| `address` | body | `object` | no | — |
