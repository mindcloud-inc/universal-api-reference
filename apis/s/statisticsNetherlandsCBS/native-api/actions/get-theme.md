# Get Theme with Statistics Netherlands CBS

Retrieves a theme from Statistics Netherlands CBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataCatalog/Themes({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Theme](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric theme ID. Required by the OData key path. |
