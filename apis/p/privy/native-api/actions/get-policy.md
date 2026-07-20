# Get Policy with Privy

Retrieves a policy from Privy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/policies/{{policyId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Policy](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Privy policy ID. |
