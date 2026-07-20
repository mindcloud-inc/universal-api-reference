# List OData Entity Records with Resco Cloud

Retrieves OData entity records from Resco Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `https://{organization}.rescocrm.com/odata/v4/:entity`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [List OData Entity Records](https://docs.resco.net/wiki/OData_service)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | path | `string` | yes | OData entity set name, for example account. |
| `$select` | query | `string` | no | Comma-separated OData properties to return. |
| `$expand` | query | `string` | no | OData expand expression. |
| `$filter` | query | `string` | no | OData filter expression. |
