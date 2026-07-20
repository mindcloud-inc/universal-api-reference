# List Role Bindings with Confluent

Retrieves role bindings from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/role-bindings`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [List Role Bindings](https://docs.confluent.io/cloud/current/api.html#tag/Role-Bindings-(iamv2)/operation/listIamV2RoleBindings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `crn_pattern` | query | `string` | yes |
| `principal` | query | `string` | no |
| `role_name` | query | `string` | no |
