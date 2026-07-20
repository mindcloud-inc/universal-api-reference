# Optimize Remote Image Direct with ShortPixel

Creates an optimized image directly from a remote URL in ShortPixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/reducer-sync.php`
- **Base URL:** `https://api.shortpixel.com`
- **Official documentation:** [Optimize Remote Image Direct](https://shortpixel.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The publicly reachable image URL to optimize and return directly. |
| `lossy` | body | `number` | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | body | `number` | no | Maximum seconds to wait for optimization before returning. |
