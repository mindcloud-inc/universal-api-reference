# Update Account with Salesflare

## Endpoint

- **Method:** `PUT`
- **Path:** `accounts/:account_id`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [Update Account](https://api.salesflare.com/docs#/Accounts/putAccountsAccount_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | The Salesflare account ID. |
| `name` | body | `string` | no | The account name. |
