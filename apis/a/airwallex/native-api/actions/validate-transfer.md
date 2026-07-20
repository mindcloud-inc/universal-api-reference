# Validate Transfer with Airwallex

Validates transfer details in Airwallex before payout creation.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/transfers/validate`
- **Base URL:** `https://api-demo.airwallex.com`
- **Official documentation:** [Validate Transfer](https://www.airwallex.com/docs/payouts/transfers/validate-a-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beneficiary_id` | body | `string` | yes | The saved Airwallex beneficiary ID to validate. |
| `transfer_amount` | body | `string` | yes | The amount to validate for payout. |
| `transfer_currency` | body | `string` | yes | The payout currency, such as USD. |
| `transfer_method` | body | `string` | yes | The payout transfer method, such as LOCAL. |
| `reason` | body | `string` | yes | The transfer purpose or payout reason. |
| `reference` | body | `string` | yes | A transfer reference visible to the payer. |
| `request_id` | body | `string` | yes | A unique idempotency key for the validation request. |
| `source_currency` | body | `string` | yes | The source wallet currency used to fund the payout. |
| `lock_rate_on_create` | body | `boolean` | yes | Whether to lock the FX rate at validation time. |
| `transfer_date` | body | `string` | yes | The scheduled transfer date in YYYY-MM-DD format. |
