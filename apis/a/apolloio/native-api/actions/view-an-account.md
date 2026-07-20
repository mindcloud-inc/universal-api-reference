# View an Account with Apollo

Retrieves an account record from Apollo.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/accounts/:id`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [View an Account](https://docs.apollo.io/reference/view-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Apollo ID for the account that you want to retrieve. To find account IDs, call the Search for Accounts endpoint and identify the `id` value for the account. Example: `6518c6184f20350001a0b9c0` |
