# Deduct Subaccount Balance with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/subaccount/deduct-balance`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Deduct Subaccount Balance](https://app.smsup.es/api/3.0/docs/subaccount/deduct-balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_name` | body | `string` | yes | Username of the subaccount. |
| `amount` | body | `number` | yes | Amount to deduct. |
