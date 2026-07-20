# Create Subcategory with Oboloo

Creates a new subcategory in Oboloo.

## Endpoint

- **Method:** `POST`
- **Path:** `/configuration/addSubCategory`
- **Base URL:** `https://mindcloudwizard20260330.oboloo.app/api`
- **Official documentation:** [Create Subcategory](https://oboloo.app/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Category identifier that this subcategory belongs to. |
| `subcategory_name` | body | `string` | yes | Name of the subcategory to create. |
