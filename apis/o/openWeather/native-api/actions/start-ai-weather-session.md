# Start AI Weather Session with OpenWeather

Starts an OpenWeather AI weather assistant session.

## Endpoint

- **Method:** `POST`
- **Path:** `/assistant/session`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Start AI Weather Session](https://openweathermap.org/api/one-call-3)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Weather-related question to ask the assistant. |
