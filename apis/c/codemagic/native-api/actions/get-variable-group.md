# Get Variable Group with Codemagic

Retrieves a specific variable group from Codemagic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/variable-groups/:variable_group_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Variable Group](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdGetGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable_group_id` | path | `string` | yes | Codemagic variable group identifier. |
