# Update License with Cryptlex

Updates an existing license in Cryptlex.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/licenses/:id`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Update License](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/patch/v3/licenses/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the license. |
| `key` | body | `string` | no | Key associated with the license. |
| `notes` | body | `string` | no | Notes to store with the license. |
| `suspended` | body | `boolean` | no | Whether to suspend the license. |
| `revoked` | body | `boolean` | no | Whether to revoke the license. |
| `userId` | body | `string` | no | User linked to the license. |
| `allowedActivations` | body | `number` | no | Allowed number of activations for the license. |
