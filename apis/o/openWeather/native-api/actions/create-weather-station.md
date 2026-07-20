# Create Weather Station with OpenWeather

Creates a weather station in your OpenWeather account.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/3.0/stations`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Create Weather Station](https://openweathermap.org/stations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | yes | External identifier for the station. |
| `name` | body | `string` | yes | Station display name. |
| `latitude` | body | `number` | yes | Station latitude. |
| `longitude` | body | `number` | yes | Station longitude. |
| `altitude` | body | `number` | yes | Station altitude in meters. |
