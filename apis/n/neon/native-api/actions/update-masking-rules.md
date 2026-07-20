# Update masking rules with Neon

Updates masking rules in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/masking_rules`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update masking rules](https://api-docs.neon.tech/reference/updatemaskingrules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `masking_rules[]` | body | `array<object>` | yes | Neon API parameter masking_rules |
