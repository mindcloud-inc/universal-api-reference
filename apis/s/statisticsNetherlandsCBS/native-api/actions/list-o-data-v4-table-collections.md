# List OData V4 Table Collections with Statistics Netherlands CBS

Retrieves OData V4 collections from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [List OData V4 Table Collections](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
