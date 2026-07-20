# Get OData V4 Dimension Group with Statistics Netherlands CBS

Retrieves a dimension group from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Groups('{{id}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Dimension Group](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimensionIdentifier` | path | `string` | yes | OData v4 dimension identifier prefix, such as WijkenEnBuurten. |
| `id` | path | `string` | yes | OData v4 dimension group id, such as WBGM. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
