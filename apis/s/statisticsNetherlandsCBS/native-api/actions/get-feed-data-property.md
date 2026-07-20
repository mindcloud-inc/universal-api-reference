# Get Feed Data Property with Statistics Netherlands CBS

Retrieves a feed data property from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/DataProperties({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Feed Data Property](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric DataProperties row ID. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, such as 83765NED. |
