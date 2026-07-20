# Create a single customField with GrowthBook

Creates a new custom field in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/custom-fields`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single customField](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The unique key for the custom field |
| `name` | body | `string` | yes | The display name of the custom field |
| `description` | body | `string` | no | — |
| `placeholder` | body | `string` | no | — |
| `defaultValue` | body | `string` | no | — |
| `type` | body | `string` | yes | The type of value this custom field will take |
| `values` | body | `string` | no | — |
| `required` | body | `boolean` | yes | — |
| `projects` | body | `list<string>` | no | — |
| `sections` | body | `list<string>` | yes | What types of objects this custom field is applicable to (feature, experiment) |
