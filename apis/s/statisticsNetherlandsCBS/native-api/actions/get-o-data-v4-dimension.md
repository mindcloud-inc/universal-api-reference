# Get OData V4 Dimension with Statistics Netherlands CBS

Retrieves a dimension from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Dimensions('{{identifier}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Dimension](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | OData v4 dimension identifier, such as WijkenEnBuurten. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
