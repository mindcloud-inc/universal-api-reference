# Patch Transaction Disbursement Method with Escrow.com

Updates a transaction disbursement method in Escrow.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/transaction/:transaction_id/disbursement_methods`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Patch Transaction Disbursement Method](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `account_name` | body | `string` | no | Name on the account receiving disbursement. |
| `account_type` | body | `string` | no | ACH account type, checking or savings. |
| `bank_aba_routing_number` | body | `string` | no | ABA routing number for ACH disbursement. |
| `bank_account_number` | body | `string` | no | Bank account number for ACH disbursement. |
| `bank_name` | body | `string` | no | Name of the bank receiving disbursement. |
| `currency` | body | `string` | no | Currency accepted by the disbursement method. |
| `bank_address` | body | `object` | no | Bank address for disbursement. |
| `beneficiary_address` | body | `object` | no | Beneficiary address for disbursement. |
| `type` | body | `string` | no | Disbursement method type, such as ach or wire_transfer. |
