# Create Contact Attribute with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts/attributes/:attributeCategory/:attributeName`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create Contact Attribute](https://developers.brevo.com/reference/create-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributeCategory` | path | `string` | yes | Attribute category such as normal, transactional, category, calculated, or global. |
| `attributeName` | path | `string` | yes | Attribute name to create. |
| `enumeration` | body | `object` | no | Array of options for category attributes. |
| `isRecurring` | body | `boolean` | no | Whether calculated values should be recurring. |
| `multiCategoryOptions` | body | `object` | no | Array of options for multiple-choice attributes. |
| `type` | body | `string` | no | Data type for normal/transactional attributes, e.g. text or multiple-choice. |
| `value` | body | `string` | no | Default/calculated value expression for calculated or global attributes. |
