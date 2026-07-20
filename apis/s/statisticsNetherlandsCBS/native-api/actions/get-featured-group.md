# Get Featured Group with Statistics Netherlands CBS

Retrieves a featured group from Statistics Netherlands CBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataCatalog/Featured({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Featured Group](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric featured group ID. Required by the OData key path. |
