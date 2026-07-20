# Get masking rules with Neon

Retrieves masking rules from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/masking_rules`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get masking rules](https://api-docs.neon.tech/reference/getmaskingrules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
