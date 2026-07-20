# Delete Virtual Account with Finmo

Deletes an existing virtual account from Finmo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/virtual-account/:virtual_account_id`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Delete Virtual Account](https://docs.finmo.net/reference/deletevirtualaccount-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `virtual_account_id` | path | `string` | yes | Virtual account identifier to delete. |
