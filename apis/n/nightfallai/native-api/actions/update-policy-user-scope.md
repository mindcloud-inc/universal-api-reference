# Update Policy User Scope with Nightfall.ai

Updates a policy user scope in Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/policy/v1/:policyID/scope/users`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Update Policy User Scope](https://help.nightfall.ai/developer-api/nightfall_apis/scope_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyID` | path | `string` | yes | The policy UUID to update. |
| `add` | body | `object` | no | Object containing users to add to policy scope. |
| `delete` | body | `object` | no | Object containing users to remove from policy scope. |
