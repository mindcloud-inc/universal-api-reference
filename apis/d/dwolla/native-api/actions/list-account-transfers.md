# List Account Transfers with Dwolla

Finds transfers for a Dwolla account by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/[:id]/transfers`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [List Account Transfers](https://developers.dwolla.com/docs/api-reference/accounts/list-and-search-transfers-for-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla account ID. |
