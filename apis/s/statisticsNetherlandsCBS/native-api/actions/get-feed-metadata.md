# Get Feed Metadata with Statistics Netherlands CBS

Retrieves feed metadata from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataFeed/odata/{{tableIdentifier}}/$metadata`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Feed Metadata](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the feed service path. |
