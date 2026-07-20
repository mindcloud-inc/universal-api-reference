# Get Data Property with Statistics Netherlands CBS

Retrieves a data property from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/DataProperties({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Data Property](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric data property row ID. Required by the OData key path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
