# Get Language Code By Id with AccuWeather

Retrieves a language code from AccuWeather by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/translations/v1/languages/id/:languageID`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Language Code By Id](https://developer.accuweather.com/core-weather/languages-translations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageID` | path | `string` | yes | Required AccuWeather language ID. |
