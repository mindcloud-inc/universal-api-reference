# Update Contact Attribute with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/contacts/attributes/:attributeCategory/:attributeName`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Contact Attribute](https://developers.brevo.com/reference/update-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributeCategory` | path | `string` | yes | Attribute category, for example normal or transactional. |
| `attributeName` | path | `string` | yes | Attribute name to update. |
| `multiCategoryOptions` | body | `object<string>` | no | Array of string options when updating a multi-category attribute. |
