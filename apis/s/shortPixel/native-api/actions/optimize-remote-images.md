# Optimize Remote Images with ShortPixel

Creates optimized image results from remote URLs in ShortPixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/reducer.php`
- **Base URL:** `https://api.shortpixel.com`
- **Official documentation:** [Optimize Remote Images](https://shortpixel.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urllist[]` | body | `array<string>` | yes | One or more publicly reachable image URLs to optimize. |
| `lossy` | body | `number` | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | body | `number` | no | Maximum seconds to wait for optimization before returning. |
