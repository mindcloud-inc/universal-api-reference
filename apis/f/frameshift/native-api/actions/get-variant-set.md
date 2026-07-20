# Get Variant Set with Frameshift

Retrieves variant set details from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/variants/sets/:variant_set_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Variant Set](https://mosaic.frameshift.io/api/#api-Variants-GetVariantSet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `variant_set_id` | path | `string` | yes | Resource identifier for the variant set to access |
| `include_variant_data` | query | `boolean` | no | If true, all data for the variants in the set will be returned. |
| `include_genotype_data` | query | `boolean` | no | If true, genotype data will be returned. |
