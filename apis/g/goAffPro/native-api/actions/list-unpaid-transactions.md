# List Unpaid Transactions with GoAffPro

Retrieves unpaid affiliate transactions from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/payments/transactions/unpaid`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Unpaid Transactions](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return unpaid transactions for this affiliate ID. |
| `group_id` | query | `string` | no | Only return unpaid transactions for this group ID. |
| `payment_method` | query | `string` | no | Only return unpaid transactions with this payment method. |
