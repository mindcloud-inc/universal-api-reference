# Get Account with Snappy

Retrieves an account from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/{accountId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Get Account](https://docs.snappy.com/reference/getaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The id of the account. |
| `companyId` | query | `string` | no | Company ID. |
