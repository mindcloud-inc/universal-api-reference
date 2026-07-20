# Update Policy Rule with Privy

Updates a rule in a Privy policy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/policies/{{policyId}}/rules/{{ruleId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Update Policy Rule](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules~1{rule_id}/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Privy policy ID. |
| `rule_id` | path | `string` | yes | Privy policy rule ID. |
