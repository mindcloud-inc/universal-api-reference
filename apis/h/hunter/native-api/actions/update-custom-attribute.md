# Update Custom Attribute with Hunter

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads_custom_attributes/:customAttributeId`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Update Custom Attribute](https://hunter.io/api-documentation/v2#update-custom-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customAttributeId` | path | `string` | yes | Identifier of the custom attribute. |
| `label` | body | `string` | yes | — |
