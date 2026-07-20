# Get Historical Weather with Pirate Weather

Retrieves historical weather from Pirate Weather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://timemachine.pirateweather.net/forecast/header-auth/:latitude,:longitude,:time`
- **Base URL:** `https://api.pirateweather.net`
- **Official documentation:** [Get Historical Weather](https://docs.pirateweather.net/en/latest/API/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `number` | yes | Latitude in decimal degrees. |
| `longitude` | path | `number` | yes | Longitude in decimal degrees. |
| `time` | path | `string` | yes | Past time as a UNIX timestamp or supported Pirate Weather time string. |
