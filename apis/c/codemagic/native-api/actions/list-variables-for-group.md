# List Variables For Group with Codemagic

Retrieves variables for a specific Codemagic variable group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/variable-groups/:variable_group_id/variables`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Variables For Group](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesGetVariables)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable_group_id` | path | `string` | yes | Codemagic variable group identifier. |
| `search` | query | `string` | no | Optional variable search string. |
