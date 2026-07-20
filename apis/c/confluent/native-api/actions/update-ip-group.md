# Update IP Group with Confluent

Updates an existing IP group in Confluent Cloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v2/ip-groups/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Update IP Group](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/updateIamV2IpGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `group_name` | body | `string` | no |
| `cidr_blocks[]` | body | `array<string>` | no |
