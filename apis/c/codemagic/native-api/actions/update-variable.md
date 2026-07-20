# Update Variable with Codemagic

Updates an existing variable in a Codemagic group.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/variable-groups/:variable_group_id/variables/:variable_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Update Variable](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesVariableIdUpdateVariable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable_group_id` | path | `string` | yes | Codemagic variable group identifier. |
| `variable_id` | path | `string` | yes | Codemagic environment variable identifier. |
| `name` | body | `string` | no | Optional new variable name. |
| `value` | body | `string` | no | Optional new variable value. |
| `secure` | body | `boolean` | no | Whether the variable should be stored securely. |
