# Create IP Filter with Confluent

Creates a new IP filter in Confluent Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v2/ip-filters`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Create IP Filter](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/createIamV2IpFilter)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter_name` | body | `string` | yes |
| `resource_group` | body | `string` | yes |
| `resource_scope` | body | `string` | no |
| `operation_groups[]` | body | `array<string>` | no |
| `ip_groups[]` | body | `array<object>` | yes |
