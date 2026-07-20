# Search Variants By Region with Frameshift

Finds variants in Frameshift by genomic region.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/variants/by-region`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Search Variants By Region](https://mosaic.frameshift.io/api/#api-Variants-GetVariantsByRegion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `chr` | query | `string` | yes | The chromosome to filter on. Use values like 1 rather than chr1. |
| `start` | query | `number` | yes | The region start to filter on. |
| `end` | query | `number` | yes | The region end to filter on. |
| `inheritance` | query | `string` | no | Optional inheritance filter. |
