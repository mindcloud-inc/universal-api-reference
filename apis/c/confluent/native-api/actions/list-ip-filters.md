# List IP Filters with Confluent

Retrieves IP filters from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/ip-filters`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [List IP Filters](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/listIamV2IpFilters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_scope` | query | `string` | no |
| `include_parent_scopes` | query | `string` | no |
