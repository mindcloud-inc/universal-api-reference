# Get Table Service Metadata with Statistics Netherlands CBS

Retrieves service metadata from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/$metadata`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Table Service Metadata](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
