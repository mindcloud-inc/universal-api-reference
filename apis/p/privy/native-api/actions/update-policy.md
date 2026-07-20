# Update Policy with Privy

Updates an existing policy in Privy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/policies/{{policyId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Update Policy](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Privy policy ID. |
