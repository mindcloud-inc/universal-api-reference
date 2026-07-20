# Create Variant Filter with Frameshift

Creates a variant filter in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/variants/filters`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Variant Filter](https://mosaic.frameshift.io/api/#api-Variant_Filters-CreateVariantFilter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `name` | body | `string` | yes | Name for the variant filter |
| `description` | body | `string` | no | Description of the variant filter |
| `filter` | body | `object` | yes | JSON describing the variant filters |
