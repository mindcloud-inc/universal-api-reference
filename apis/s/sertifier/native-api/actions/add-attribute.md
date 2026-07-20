# Add Attribute with Sertifier

Creates a new attribute in Sertifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/attribute`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Add Attribute](https://sertifier.docs.apiary.io/reference/attribute/add-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Internal title for the attribute. |
| `type` | body | `number` | yes | Attribute value type: 1 text, 2 date, 3 number. |
