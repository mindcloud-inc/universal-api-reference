# List Transfers with Airwallex

Retrieves payout transfer records from Airwallex.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/transfers`
- **Base URL:** `https://api-demo.airwallex.com`
- **Official documentation:** [List Transfers](https://www.airwallex.com/docs/payouts/transfers/create-a-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_created_at` | query | `date` | no | Inclusive lower bound for transfer creation date in YYYY-MM-DD format. |
| `to_created_at` | query | `date` | no | Inclusive upper bound for transfer creation date in YYYY-MM-DD format. |
| `transfer_currency` | query | `string` | no | Filter transfers by payout currency. |
| `status` | query | `string` | no | Filter transfers by transfer status. |
