# Update Account with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/account`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Account](https://developer.surecart.com/api-reference/accounts/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account.name` | body | `string` | no | The account display name. |
| `account.currency` | body | `string` | no | The default currency for the account. |
