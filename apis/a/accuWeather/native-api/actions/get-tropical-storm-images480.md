# Get Radar And Satellite Imagery 480 with AccuWeather

Retrieves 480px radar and satellite imagery from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/imagery/v1/maps/radsat/:resolution/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Radar And Satellite Imagery 480](https://developer.accuweather.com/core-weather/imagery)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
| `resolution` | path | `string` | yes | Required image size. |
