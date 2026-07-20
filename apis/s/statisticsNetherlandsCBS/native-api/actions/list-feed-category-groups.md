# List Feed Category Groups with Statistics Netherlands CBS

Retrieves feed category groups from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/CategoryGroups`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List Feed Category Groups](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, such as 83765NED. |
