# Update User with Permit.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/facts/:projId/:envId/users/:userId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Update User](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `userId` | path | `string` | yes | Permit user identifier. |
| `email` | body | `string` | no | Updated user email address. |
| `first_name` | body | `string` | no | Updated user first name. |
| `last_name` | body | `string` | no | Updated user last name. |
| `attributes` | body | `object` | no | Updated custom user attributes object. |
