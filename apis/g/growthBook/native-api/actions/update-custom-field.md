# Update a single customField with GrowthBook

Updates an existing custom field in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/custom-fields/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single customField](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | The display name of the custom field |
| `description` | body | `string` | no | — |
| `placeholder` | body | `string` | no | — |
| `defaultValue` | body | `string` | no | — |
| `values` | body | `string` | no | — |
| `required` | body | `boolean` | no | — |
| `projects` | body | `list<string>` | no | — |
| `sections` | body | `list<string>` | no | What types of objects this custom field is applicable to (feature, experiment) |
| `active` | body | `boolean` | no | — |
