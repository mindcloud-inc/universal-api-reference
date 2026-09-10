# Get Customers with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/customers`
- **Base URL:** `https://{baseUrl}/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unit` | query | `string` | no | — |
| `city` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `country` | query | `string` | no | — |
| `phone` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `modifiedBefore` | query | `string` | no | — |
| `street` | query | `string` | no | — |
| `zip` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | — |
| `active` | query | `boolean` | no | — |
| `ids` | query | `string` | no | — |
| `excludeAccountingChangesFromModifiedDateRange` | query | `boolean` | no | Excludes accounting changes such as balance adjustments from the modified date range. |
| `externalDataApplicationGuid` | query | `string` | no | — |
| `externalDataKey` | query | `string` | no | — |
| `externalDataValues` | query | `string` | no | — |
