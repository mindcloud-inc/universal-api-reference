# Get Variable with Codemagic

Retrieves a specific variable from a Codemagic group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/variable-groups/:variable_group_id/variables/:variable_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Variable](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesVariableIdGetVariable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable_group_id` | path | `string` | yes | Codemagic variable group identifier. |
| `variable_id` | path | `string` | yes | Codemagic environment variable identifier. |
