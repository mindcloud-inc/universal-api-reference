# Update Variable Group with Codemagic

Updates an existing variable group in Codemagic.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/variable-groups/:variable_group_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Update Variable Group](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdUpdateGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable_group_id` | path | `string` | yes | Codemagic variable group identifier. |
| `name` | body | `string` | no | Optional new variable group name. |
| `advanced_security` | body | `object` | no | Optional advanced security object for team variable groups. |
