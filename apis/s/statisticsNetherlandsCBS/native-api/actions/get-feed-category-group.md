# Get Feed Category Group with Statistics Netherlands CBS

Retrieves a feed category group from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/CategoryGroups({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Feed Category Group](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric CategoryGroups row ID. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, such as 83765NED. |
