# Read Role Binding with Confluent

Retrieves a role binding from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/role-bindings/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Read Role Binding](https://docs.confluent.io/cloud/current/api.html#tag/Role-Bindings-(iamv2)/operation/getIamV2RoleBinding)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
