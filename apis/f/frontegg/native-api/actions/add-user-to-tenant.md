# Add User To Tenant with Frontegg

Adds a user to an account in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/users/v1/:userId/tenant`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Add User To Tenant](https://developers.frontegg.com/ciam/api/identity/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID to add to a tenant. |
| `tenantId` | body | `string` | yes | Tenant ID to add the user to. |
| `skipInviteEmail` | body | `boolean` | no | Skip the invitation email when true. |
| `validateTenantExist` | body | `boolean` | no | Validate the tenant before adding the user. |
