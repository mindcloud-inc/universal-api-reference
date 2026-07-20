# Get Bookings with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/bookings`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Bookings](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Bookings_Create)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `ids` | query | `string` | no |
| `externalId` | query | `string` | no |
