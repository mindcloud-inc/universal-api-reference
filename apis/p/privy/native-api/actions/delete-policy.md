# Delete Policy with Privy

Deletes an existing policy from Privy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/policies/{{policyId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Delete Policy](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Privy policy ID. |
