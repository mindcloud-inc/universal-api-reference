# Get OData V4 Measure Code with Statistics Netherlands CBS

Retrieves a measure code from a Statistics Netherlands CBS dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureCodes('{{identifier}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Measure Code](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | OData v4 measure code identifier, such as GM000C. |
| `tableIdentifier` | path | `string` | yes | CBS table identifier, such as 83765NED. |
