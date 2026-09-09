# List Customers with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Customer`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Customers](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | Comma-separated entity fields to return. |
| `$expand` | query | `string` | no | Comma-separated detail or linked entities to expand. |
| `$filter` | query | `string` | no | Acumatica OData filter expression used to qualify returned records. |
| `$custom` | query | `string` | no | Comma-separated custom fields to return. |
