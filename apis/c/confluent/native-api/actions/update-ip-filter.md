# Update IP Filter with Confluent

Updates an existing IP filter in Confluent Cloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v2/ip-filters/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Update IP Filter](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/updateIamV2IpFilter)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `filter_name` | body | `string` | no |
| `resource_group` | body | `string` | no |
| `resource_scope` | body | `string` | no |
| `operation_groups[]` | body | `array<string>` | no |
| `ip_groups[]` | body | `array<object>` | no |
