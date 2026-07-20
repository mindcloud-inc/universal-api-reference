# Get OData V4 Table Properties with Statistics Netherlands CBS

Retrieves table properties from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Properties`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Table Properties](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
