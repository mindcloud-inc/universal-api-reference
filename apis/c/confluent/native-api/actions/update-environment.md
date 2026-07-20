# Update Environment with Confluent

Updates an existing environment in Confluent Cloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/org/v2/environments/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Update Environment](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/updateOrgV2Environment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `display_name` | body | `string` | no |
| `stream_governance_config.package` | body | `string` | no |
