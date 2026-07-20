# Bulk Import Variables For Group with Codemagic

Bulk imports variables into a Codemagic variable group.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/variable-groups/:variable_group_id/variables`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Bulk Import Variables For Group](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesBulkImport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variable_group_id` | path | `string` | yes | Codemagic variable group identifier. |
| `secure` | body | `boolean` | yes | Whether imported variables should be stored securely. |
| `variables[]` | body | `array<object>` | yes | Variables to import. Each item includes name and value. |
