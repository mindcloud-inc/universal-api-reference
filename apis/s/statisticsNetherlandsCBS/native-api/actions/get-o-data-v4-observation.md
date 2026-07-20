# Get OData V4 Observation with Statistics Netherlands CBS

Retrieves an observation from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Observations({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Observation](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | OData v4 observation id, such as 1. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
