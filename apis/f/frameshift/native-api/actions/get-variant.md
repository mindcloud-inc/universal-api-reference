# Get Variant with Frameshift

Retrieves detailed variant information from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/variants/:variant_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Variant](https://mosaic.frameshift.io/api/#api-Variants-GetVariant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `variant_id` | path | `string` | yes | Resource identifier for the variant to access |
| `include_annotation_data` | query | `boolean` | no | If true, the annotations for the variant will be included in the response |
| `include_genotype_data` | query | `boolean` | no | If true, genotype data such as which samples are het or hom for this variant will be included in the response |
