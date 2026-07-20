# Update Variant Filter with Frameshift

Updates an existing variant filter in Frameshift.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/projects/:project_id/variants/filters/:variant_filter_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Update Variant Filter](https://mosaic.frameshift.io/api/#api-Variant_Filters-UpdateVariantFilter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `variant_filter_id` | path | `string` | yes | Resource identifier for the variant filter to access |
| `name` | body | `string` | no | Name for the variant filter |
| `description` | body | `string` | no | Description of the variant filter |
| `filter` | body | `object` | no | JSON describing the variant filters |
