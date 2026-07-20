# Get Table Theme Link with Statistics Netherlands CBS

Retrieves a table theme link from Statistics Netherlands CBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataCatalog/Tables_Themes({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Table Theme Link](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Tables_Themes relationship ID. |
