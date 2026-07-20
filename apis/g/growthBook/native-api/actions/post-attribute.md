# Create a new attribute with GrowthBook

Creates a new attribute in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/attributes`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a new attribute](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property` | body | `string` | yes | The attribute property |
| `datatype` | body | `string` | yes | The attribute datatype |
| `description` | body | `string` | no | The description of the new attribute |
| `archived` | body | `boolean` | no | The attribute is archived |
| `hashAttribute` | body | `boolean` | no | Shall the attribute be hashed |
| `enum` | body | `string` | no | — |
| `format` | body | `string` | no | The attribute's format |
| `projects` | body | `list<string>` | no | — |
| `tags` | body | `list<string>` | no | — |
