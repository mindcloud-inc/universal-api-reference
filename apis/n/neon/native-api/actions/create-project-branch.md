# Create branch with Neon

Creates a branch in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create branch](https://api-docs.neon.tech/reference/createprojectbranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoints[]` | body | `array<object>` | no | Neon API parameter endpoints |
| `branch` | body | `object` | no | Neon API parameter branch |
| `annotation_value` | body | `object` | no | Neon API parameter annotation_value |
