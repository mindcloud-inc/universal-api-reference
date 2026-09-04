# List Sales Orders with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Sales Orders](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-the-List-of-Records-in-Batches)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$select` | query | `string` | no |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
