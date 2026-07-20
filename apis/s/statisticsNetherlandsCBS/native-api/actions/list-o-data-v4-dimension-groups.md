# List OData V4 Dimension Groups with Statistics Netherlands CBS

Retrieves dimension groups from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Groups`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List OData V4 Dimension Groups](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimensionIdentifier` | path | `string` | yes | OData v4 dimension identifier prefix, such as WijkenEnBuurten. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
