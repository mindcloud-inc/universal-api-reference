# Get Technicians with ServiceTitan

Retrieves technicians from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `settings/v2/tenant/{tenant}/technicians`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Technicians](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=Technicians_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | — |
| `includeTotal` | query | `boolean` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `userIds` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | — |
| `externalDataApplicationGuid` | query | `string` | no | — |
| `ids` | query | `string` | no | Send multiple values as a string. |
| `modifiedBefore` | query | `string` | no | — |
