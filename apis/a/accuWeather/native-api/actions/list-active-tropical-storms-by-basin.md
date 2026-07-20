# List Active Tropical Storms By Basin with AccuWeather

Lists active tropical storms in AccuWeather by basin.

## Endpoint

- **Method:** `GET`
- **Path:** `/tropical/v1/gov/storms/active/:basin`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [List Active Tropical Storms By Basin](https://developer.accuweather.com/core-weather/active)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basin` | path | `string` | yes | Required tropical basin code. |
