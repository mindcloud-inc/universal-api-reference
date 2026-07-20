# Disable User Account (Tenant) with Frontegg

Disables a user for an account in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/tenants/users/v1/:userId/disable`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Disable User Account (Tenant)](https://developers.frontegg.com/ciam/api/identity/user-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID to disable for the tenant. |
