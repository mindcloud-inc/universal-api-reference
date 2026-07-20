# Get Feed Table Info with Statistics Netherlands CBS

Retrieves feed table info from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/TableInfos({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Feed Table Info](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric TableInfos row ID. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, such as 83765NED. |
