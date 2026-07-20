# Get OData V4 Dimension Code with Statistics Netherlands CBS

Retrieves a dimension code from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Codes('{{identifier}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Dimension Code](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimensionIdentifier` | path | `string` | yes | OData v4 dimension identifier prefix, such as WijkenEnBuurten. |
| `identifier` | path | `string` | yes | OData v4 dimension code identifier, such as NL00. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
