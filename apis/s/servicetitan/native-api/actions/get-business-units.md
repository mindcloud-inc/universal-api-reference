# Get Business Units with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `settings/v2/tenant/{tenant}/business-units`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Business Units](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=BusinessUnits_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | query | `boolean` | no |
| `includeTotal` | query | `boolean` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `name` | query | `string` | no |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `externalDataApplicationGuid` | query | `string` | no |
| `ids` | query | `string` | no |
| `modifiedBefore` | query | `string` | no |
