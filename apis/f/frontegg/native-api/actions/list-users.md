# List Users with Frontegg

Finds users in your Frontegg environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/resources/users/v3`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [List Users](https://developers.frontegg.com/ciam/api/identity/user-management)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_limit` | query | `number` | no | Maximum number of users to return (default 50, maximum 200). |
| `_offset` | query | `number` | no | Page number to retrieve, starting at 0. |
| `_email` | query | `string` | no | Filter users by email. |
| `_tenantId` | query | `string` | no | Filter users by tenant ID. |
| `_sortBy` | query | `string` | no | Sort by createdAt, name, email, id, verified, isLocked, provider, or tenantId. |
| `_order` | query | `string` | no | Sort order: ASC or DESC. |
| `_namePrefix` | query | `string` | no | Filter users by name prefix. |
| `_identifier` | query | `string` | no | Filter by identifier prefix. Must be used with Identifier Type. |
| `_identifierType` | query | `string` | no | Identifier type: email, phoneNumber, or username. |
| `_includeSubTenants` | query | `boolean` | no | Include sub-tenants when searching users. |
| `ids` | query | `string` | no | Specific user IDs to retrieve. |
| `_externalIds` | query | `string` | no | Filter users by external IDs. |
