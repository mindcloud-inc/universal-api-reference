# Get Bank Account Details with Kiwili

Retrieves details for a bank account in Kiwili.

## Endpoint

- **Method:** `GET`
- **Path:** `/bankaccount/:bank_account_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Get Bank Account Details](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bank_account_id` | path | `string` | yes | The Kiwili bank account ID. Use the string 0 for the default record when needed. |
