# Check Uploaded Optimization Status with ShortPixel

Retrieves uploaded image optimization status from ShortPixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/post-reducer.php`
- **Base URL:** `https://api.shortpixel.com`
- **Official documentation:** [Check Uploaded Optimization Status](https://shortpixel.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_urls[]` | body | `array<string>` | yes | One or more temporary OriginalURL values returned by the upload action for pending optimizations. |
| `lossy` | body | `number` | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | body | `number` | no | Maximum seconds to wait before returning the latest optimization status. |
