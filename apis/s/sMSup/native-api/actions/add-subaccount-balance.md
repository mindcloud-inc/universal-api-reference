# Add Subaccount Balance with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/subaccount/add-balance`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Add Subaccount Balance](https://app.smsup.es/api/3.0/docs/subaccount/add-balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_name` | body | `string` | yes | Username of the subaccount. |
| `amount` | body | `number` | yes | Amount to add. |
