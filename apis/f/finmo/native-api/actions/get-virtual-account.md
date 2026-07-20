# Get Virtual Account with Finmo

Finds a virtual account in Finmo by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/virtual-account/:virtual_account_id`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Get Virtual Account](https://docs.finmo.net/reference/getvirtualaccountbyid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `virtual_account_id` | path | `string` | yes | Virtual account identifier to retrieve. |
| `include_deleted` | query | `boolean` | no | Include deleted virtual accounts in the lookup. |
