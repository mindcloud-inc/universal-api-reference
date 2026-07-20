# Create Account with Snappy

Creates a new account in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Create Account](https://docs.snappy.com/reference/createaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The account name. |
| `billingMethod` | body | `object` | yes | Billing method object for the account. |
| `companyId` | query | `string` | no | Company ID. |
