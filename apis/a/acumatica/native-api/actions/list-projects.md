# List Projects with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/:wse/:version/Project`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Projects](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-Records-with-Attributes)

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
| `wse` | path | `string` | yes | — |
| `version` | path | `string` | yes | — |
| `$expand` | query | `string` | no | Use the $expand parameter to specify the linked and detail entities that should be expanded. By default, no linked or detail entities are expanded; that is, only fields of the top-level entity are returned. You need to explicitly specify each linked or detail entity to be expanded. |
| `$select` | query | `string` | no | When you retrieve records from Acumatica ERP by using the contract-based REST API, you use the $select parameter to specify the fields of the entity to be returned from Acumatica ERP. By default, all fields of the entity are returned. |
| `$filter` | query | `string` | no | — |
