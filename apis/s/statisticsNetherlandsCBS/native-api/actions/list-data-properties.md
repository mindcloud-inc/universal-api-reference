# List Data Properties with Statistics Netherlands CBS

Retrieves data properties from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/DataProperties`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List Data Properties](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
