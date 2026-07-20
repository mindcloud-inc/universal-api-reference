# Create Environment with Confluent

Creates a new environment in Confluent Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/org/v2/environments`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Create Environment](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/createOrgV2Environment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `display_name` | body | `string` | yes |
| `stream_governance_config.package` | body | `string` | no |
