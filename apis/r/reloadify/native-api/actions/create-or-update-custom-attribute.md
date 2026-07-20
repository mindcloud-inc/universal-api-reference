# Create Or Update Custom Attribute with Reloadify

Creates or updates a custom attribute in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/custom_attributes`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Custom Attribute](https://app.reloadify.com/api-docs/index.html#/custom_attributes/putV2CustomAttributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_attribute.name` | body | `string` | yes | Custom attribute name. |
| `custom_attribute.description` | body | `string` | yes | Custom attribute description. |
| `custom_attribute.datatype` | body | `string` | yes | Datatype: string, integer, float, or boolean. |
| `custom_attribute.resource` | body | `string` | yes | Resource: profile, product, order, shopping_cart, category, review, variant, or brand. |
