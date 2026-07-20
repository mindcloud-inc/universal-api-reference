# List OData V4 Observations with Statistics Netherlands CBS

Retrieves observations from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Observations`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List OData V4 Observations](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
