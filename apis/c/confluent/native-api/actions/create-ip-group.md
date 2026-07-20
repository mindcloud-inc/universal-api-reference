# Create IP Group with Confluent

Creates a new IP group in Confluent Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v2/ip-groups`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Create IP Group](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/createIamV2IpGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_name` | body | `string` | yes |
| `cidr_blocks[]` | body | `array<string>` | yes |
