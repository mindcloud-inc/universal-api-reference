# Resume AI Weather Session with OpenWeather

Continues an OpenWeather AI weather assistant session.

## Endpoint

- **Method:** `POST`
- **Path:** `/assistant/session/:sessionId`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Resume AI Weather Session](https://openweathermap.org/api/one-call-3)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | AI assistant session identifier. |
| `prompt` | body | `string` | yes | Follow-up weather-related question. |
