# Create Custom Attribute with Zixflow

Creates a new custom attribute in Zixflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/attributes/:target/:targetId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Create Custom Attribute](https://docs.zixflow.com/api-reference/attributes/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | path | `string` | yes | Target resource type for attributes. |
| `targetId` | path | `string` | yes | Target resource identifier for attributes. |
| `apiKeyName` | body | `string` | yes | Attribute API key name. |
| `inputType` | body | `string` | yes | Attribute input type. |
| `name` | body | `string` | yes | Attribute display name. |
| `config` | body | `object` | yes | Attribute configuration object. |
| `defaultValue` | body | `string` | no | Default value for the attribute. |
| `description` | body | `string` | no | Attribute description. |
| `isEditable` | body | `boolean` | no | Whether the attribute is editable. |
| `isMultiSelect` | body | `boolean` | no | Whether multiple values can be selected. |
| `isRequired` | body | `boolean` | no | Whether the attribute is required. |
| `isUnique` | body | `boolean` | no | Whether the attribute must be unique. |
| `validation` | body | `string` | no | Validation mode. |
