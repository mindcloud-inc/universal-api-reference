# Update an attribute with GrowthBook

Updates an existing attribute in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/attributes/:property`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update an attribute](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property` | path | `string` | yes | The attribute property |
| `datatype` | body | `string` | no | The attribute datatype |
| `description` | body | `string` | no | The description of the new attribute |
| `archived` | body | `boolean` | no | The attribute is archived |
| `hashAttribute` | body | `boolean` | no | Shall the attribute be hashed |
| `enum` | body | `string` | no | — |
| `format` | body | `string` | no | The attribute's format |
| `projects` | body | `list<string>` | no | — |
| `tags` | body | `list<string>` | no | — |
