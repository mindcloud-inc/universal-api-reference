# List User Roles with Rossum

Retrieves user roles from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List User Roles](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter user roles by name. |
| `ordering` | query | `string` | no | Ordering expression, for example name or -name. |
