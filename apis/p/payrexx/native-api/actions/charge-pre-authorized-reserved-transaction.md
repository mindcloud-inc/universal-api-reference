# Charge Pre-Authorized Reserved Transaction with Payrexx

Charges a pre-authorized or reserved transaction in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Transaction/:id/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Charge Pre-Authorized Reserved Transaction](https://developers.payrexx.com/reference/charge-a-pre-authorized-reserved-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the transaction to charge. |
| `amount` | body | `number` | no | Amount for charge in cents. |
| `purpose` | body | `string` | no | The purpose of the charge. |
| `referenceId` | body | `string` | no | Reference ID for charged transaction. |
| `payoutDescriptor` | body | `string` | no | Payout descriptor added to the payout statement. |
