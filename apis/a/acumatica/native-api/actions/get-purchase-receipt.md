# List Purchase Receipts with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/PurchaseReceipt`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Purchase Receipts](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-by-Conditions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | Comma-separated entity fields to return. |
| `$expand` | query | `string` | no | Comma-separated detail or linked entities to expand. |
| `$filter` | query | `string` | no | Acumatica OData filter expression used to qualify returned records. |
| `$custom` | query | `string` | no | Comma-separated custom fields to return. |
