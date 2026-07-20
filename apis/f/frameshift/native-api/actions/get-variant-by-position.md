# Get Variant By Position with Frameshift

Retrieves a variant from Frameshift by position.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/variants/position/:chr::start`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Variant By Position](https://mosaic.frameshift.io/api/#api-Variants-GetVariantByPosition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `chr` | path | `string` | yes | The chromosome position to fetch |
| `start` | path | `number` | yes | The start position to fetch |
