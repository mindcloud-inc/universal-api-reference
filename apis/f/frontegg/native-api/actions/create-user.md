# Create User with Frontegg

Creates a new user in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/vendor-only/users/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Create User](https://developers.frontegg.com/ciam/api/identity/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenantId` | body | `string` | yes | Tenant ID that the user belongs to. |
| `email` | body | `string` | yes | User email address. |
| `name` | body | `string` | yes | Full name for the user. |
| `roleIds[]` | body | `array<string>` | yes | Role IDs to assign to the user. |
| `password` | body | `string` | no | Optional password for the new user. |
| `username` | body | `string` | no | Optional username when email is omitted. |
