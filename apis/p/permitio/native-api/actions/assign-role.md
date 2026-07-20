# Assign Role with Permit.io

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/facts/:projId/:envId/role_assignments`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Assign Role](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `role` | body | `string` | yes | Role key to assign. |
| `user` | body | `string` | yes | User key receiving the assignment. |
| `tenant` | body | `string` | no | Tenant receiving the assignment, when applicable. |
| `resource_instance` | body | `string` | no | Resource instance receiving the assignment, when applicable. |
