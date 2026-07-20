# Update Custom Attribute with Zixflow

Updates an existing custom attribute in Zixflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/attributes/:target/:targetId/:attributeId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Update Custom Attribute](https://docs.zixflow.com/api-reference/attributes/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | path | `string` | yes | Target resource type for attributes. |
| `targetId` | path | `string` | yes | Target resource identifier for attributes. |
| `attributeId` | path | `string` | yes | Attribute identifier. |
| `apiKeyName` | body | `string` | no | Attribute API key name. |
| `inputType` | body | `string` | no | Attribute input type. |
| `name` | body | `string` | no | Attribute display name. |
| `config` | body | `object` | no | Attribute configuration object. |
| `defaultValue` | body | `string` | no | Default value for the attribute. |
| `description` | body | `string` | no | Attribute description. |
| `isEditable` | body | `boolean` | no | — |
| `isMultiSelect` | body | `boolean` | no | — |
| `isRequired` | body | `boolean` | no | — |
| `isUnique` | body | `boolean` | no | — |
| `validation` | body | `string` | no | — |
