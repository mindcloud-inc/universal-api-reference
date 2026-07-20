# Get Feed Resource Row with Statistics Netherlands CBS

Retrieves a feed resource row from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/{{resourceName}}('{{key}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Feed Resource Row](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | The string Key value for the row in the named feed resource. |
| `resourceName` | path | `string` | yes | Named entity set in the feed service, such as a dimension resource. Required by the service path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the feed service path. |
