# List OData V4 Dimensions with Statistics Netherlands CBS

Retrieves dimensions from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Dimensions`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List OData V4 Dimensions](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
