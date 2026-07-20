# Get OData V4 Table Metadata with Statistics Netherlands CBS

Retrieves OData V4 metadata from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/$metadata`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Table Metadata](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
