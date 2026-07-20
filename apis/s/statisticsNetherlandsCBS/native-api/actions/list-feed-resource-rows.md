# List Feed Resource Rows with Statistics Netherlands CBS

Retrieves feed resource rows from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/{{resourceName}}`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List Feed Resource Rows](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Named entity set in the feed service, such as a dimension resource. Required by the service path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the feed service path. |
