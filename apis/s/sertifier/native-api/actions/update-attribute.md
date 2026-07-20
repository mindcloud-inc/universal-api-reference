# Update Attribute with Sertifier

Updates an existing attribute in Sertifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/attribute/:attributeId`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Update Attribute](https://sertifier.docs.apiary.io/reference/attribute/update-delete-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attribute_id` | path | `string` | yes | ID of the attribute to update. |
| `title` | body | `string` | no | Updated internal title for the attribute. |
| `type` | body | `number` | no | Updated attribute value type: 1 text, 2 date, 3 number. |
