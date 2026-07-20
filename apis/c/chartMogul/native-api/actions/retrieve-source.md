# Retrieve Source with ChartMogul

Retrieves a source from ChartMogul.

## Endpoint

- **Method:** `GET`
- **Path:** `/data_sources/:dataSourceUuid`
- **Base URL:** `https://api.chartmogul.com/v1`
- **Official documentation:** [Retrieve Source](https://dev.chartmogul.com/reference/sources/retrieve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSourceUuid` | path | `string` | yes | The ChartMogul UUID of the data source to retrieve. |
