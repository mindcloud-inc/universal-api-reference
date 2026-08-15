# List Customers With External Data with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/customers`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Customers With External Data](https://developer.servicetitan.io/docs/apis/tenant-crm-v2/endpoints/Customers_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | — |
| `country` | query | `string` | no | — |
| `phone` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `unit` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `street` | query | `string` | no | — |
| `zip` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | — |
| `active` | query | `boolean` | no | — |
| `ids` | query | `string` | no | — |
| `excludeAccountingChangesFromModifiedDateRange` | query | `boolean` | no | Excludes accounting changes such as balance adjustments from the modified date range. |
| `externalDataApplicationGuid` | query | `string` | no | Returns customer records with external data for this application GUID. |
