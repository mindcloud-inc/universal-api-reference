# Create Transfer with Airwallex

Creates a new payout transfer in Airwallex.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/transfers/create`
- **Base URL:** `https://api-demo.airwallex.com`
- **Official documentation:** [Create Transfer](https://www.airwallex.com/docs/payouts/transfers/create-a-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beneficiary_id` | body | `string` | yes | The saved Airwallex beneficiary ID to pay. |
| `transfer_amount` | body | `string` | yes | The amount to send to the beneficiary. |
| `transfer_currency` | body | `string` | yes | The payout currency, such as USD. |
| `transfer_method` | body | `string` | yes | The payout transfer method, such as LOCAL. |
| `reason` | body | `string` | yes | The transfer purpose or payout reason. |
| `reference` | body | `string` | yes | A transfer reference visible to the payer. |
| `request_id` | body | `string` | yes | A unique idempotency key for the transfer request. |
| `source_currency` | body | `string` | yes | The source wallet currency used to fund the payout. |
| `lock_rate_on_create` | body | `boolean` | yes | Whether to lock the FX rate at creation time. |
| `transfer_date` | body | `string` | yes | The scheduled transfer date in YYYY-MM-DD format. |
