# Get Table Info with Statistics Netherlands CBS

Retrieves table info from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/TableInfos({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Table Info](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric TableInfos row ID. Required by the OData key path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
