# List Invoices with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Invoice`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Invoices](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | Comma-separated entity fields to return. |
| `$expand` | query | `string` | no | Comma-separated detail or linked entities to expand. |
| `$filter` | query | `string` | no | Acumatica OData filter expression used to qualify returned invoices. For decimal fields such as Balance, use numeric literals with the m suffix, for example Balance gt 0m to return invoices with a positive balance. Using Balance gt 0 can fail with "Type conversions not supported". |
| `$custom` | query | `string` | no | Comma-separated custom fields to return. |
