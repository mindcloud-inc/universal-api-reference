# List Standard Resource Rows with Statistics Netherlands CBS

Retrieves standard resource rows from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/{{resourceName}}`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List Standard Resource Rows](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Named entity set in the table service, such as a dimension resource. Required by the service path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
