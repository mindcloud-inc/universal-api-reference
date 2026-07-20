# Check Remote Optimization Status with ShortPixel

Retrieves remote image optimization status from ShortPixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/reducer.php`
- **Base URL:** `https://api.shortpixel.com`
- **Official documentation:** [Check Remote Optimization Status](https://shortpixel.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urllist[]` | body | `array<string>` | yes | One or more temporary OriginalURL values returned by ShortPixel for pending optimizations. |
| `wait` | body | `number` | no | Maximum seconds to wait before returning the latest optimization status. |
