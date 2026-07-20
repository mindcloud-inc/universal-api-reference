# Get Feed Typed Data Row with Statistics Netherlands CBS

Retrieves a feed typed data row from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/TypedDataSet({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Feed Typed Data Row](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric typed feed row ID. Required by the OData key path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the feed service path. |
