# Create a Custom Field with Apollo

Creates a new custom field in Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/fields`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Create a Custom Field](https://docs.apollo.io/reference/create-a-custom-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | no | Name of the custom field you want to create. Example: `Test Name` |
| `modality` | body | `string` | no | The modality of the custom field you want to create. Example: `contact` |
| `type` | body | `string` | no | What kind of custom field you want to create. Example: `textarea` |
| `meta` | body | `object` | no | — |
| `meta.max_length` | body | `number` | no | — |
