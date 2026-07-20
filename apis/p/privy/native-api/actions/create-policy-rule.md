# Create Policy Rule with Privy

Creates a new rule for a Privy policy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/policies/{{policyId}}/rules`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Create Policy Rule](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Privy policy ID. |
