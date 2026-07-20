# Get Table with Statistics Netherlands CBS

Retrieves a table from Statistics Netherlands CBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataCatalog/Tables({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Table](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric CBS catalog table ID. Required by the OData key path. |
