# List Account Funding Sources with Dwolla

Retrieves funding sources for a Dwolla account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/[:id]/funding-sources`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [List Account Funding Sources](https://developers.dwolla.com/docs/api-reference/accounts/list-funding-sources-for-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla account ID. |
