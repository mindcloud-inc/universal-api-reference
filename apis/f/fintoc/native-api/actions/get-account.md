# Get Account with Fintoc

Retrieves an account from Fintoc.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/accounts/:account_id`
- **Base URL:** `https://api.fintoc.com`
- **Official documentation:** [Get Account](https://docs.fintoc.com/reference/retrieve-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | Fintoc account identifier (for example `acc_...`). |
