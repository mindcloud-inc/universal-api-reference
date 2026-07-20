# List Memberships with ServiceTitan

Retrieves customer memberships from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `memberships/v2/tenant/{tenant}/memberships`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Memberships](https://developer.servicetitan.io/api-details/#api=tenant-memberships-v2&operation=CustomerMemberships_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerIds` | query | `string` | no |
| `active` | query | `string` | no |
| `billingFrequency` | query | `string` | no |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `duration` | query | `number` | no |
| `ids` | query | `string` | no |
| `includeTotal` | query | `boolean` | no |
| `modifiedBefore` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `status` | query | `string` | no |
