# Search Google Trends with HasData

Retrieves Google Trends results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google-trends/search`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google Trends](https://docs.hasdata.com/apis/google-trends/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataType` | query | `string` | no | Trend data type, such as timeseries or geoMap. |
| `date` | query | `string` | no | Date range or shortcut such as today 12-m. |
| `geo` | query | `string` | no | Geographic region code for Google Trends. |
| `q` | query | `string` | yes | Search term for Google Trends. |
