# Update Policy Domain Scope with Nightfall.ai

Updates a policy domain scope in Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/policy/v1/:policyID/scope/domains`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Update Policy Domain Scope](https://help.nightfall.ai/developer-api/nightfall_apis/scope_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyID` | path | `string` | yes | The policy UUID to update. |
| `add` | body | `object` | no | Object containing domains to add to policy scope. |
| `delete` | body | `object` | no | Object containing domains to remove from policy scope. |
