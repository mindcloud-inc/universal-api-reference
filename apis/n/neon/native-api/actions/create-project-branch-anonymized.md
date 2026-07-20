# Create anonymized branch with Neon

Creates an anonymized branch in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branch_anonymized`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create anonymized branch](https://api-docs.neon.tech/reference/createprojectbranchanonymized)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `annotation_value` | body | `object` | no | Neon API parameter annotation_value |
| `branch_create` | body | `object` | no | Neon API parameter branch_create |
| `masking_rules[]` | body | `array<object>` | no | Neon API parameter masking_rules |
| `start_anonymization` | body | `boolean` | no | Neon API parameter start_anonymization |
