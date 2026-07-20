# Get OData V4 Measure Group with Statistics Netherlands CBS

Retrieves a measure group from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureGroups('{{id}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Measure Group](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | OData v4 measure group id, such as R00000. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
