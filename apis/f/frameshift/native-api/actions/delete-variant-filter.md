# Delete Variant Filter with Frameshift

Deletes an existing variant filter from Frameshift.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/projects/:project_id/variants/filters/:variant_filter_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Delete Variant Filter](https://mosaic.frameshift.io/api/#api-Variant_Filters-DeleteVariantFilter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `variant_filter_id` | path | `string` | yes | Resource identifier for the variant filter to access |
