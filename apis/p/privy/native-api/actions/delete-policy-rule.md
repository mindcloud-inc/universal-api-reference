# Delete Policy Rule with Privy

Deletes a rule from a Privy policy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/policies/{{policyId}}/rules/{{ruleId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Delete Policy Rule](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules~1{rule_id}/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Privy policy ID. |
| `rule_id` | path | `string` | yes | Privy policy rule ID. |
