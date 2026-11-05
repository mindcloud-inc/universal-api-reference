# Get AP Credits with ServiceTitan

Retrieves AP credits from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/ap-credits`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get AP Credits](https://developer.servicetitan.io/docs/api-resources-accounting/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | — |
| `modifiedBefore` | query | `string` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `syncStatuses` | query | `string` | no | Pending - Posted - Exported - PostedAndExported |
