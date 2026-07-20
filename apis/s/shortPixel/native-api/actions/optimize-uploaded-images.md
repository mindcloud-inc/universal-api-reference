# Optimize Uploaded Images with ShortPixel

Creates optimized image results from uploaded files in ShortPixel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/post-reducer.php`
- **Base URL:** `https://api.shortpixel.com`
- **Official documentation:** [Optimize Uploaded Images](https://shortpixel.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file1` | body | `file` | yes | The local image file to upload for optimization. |
| `file_paths` | body | `object` | yes | JSON object whose keys match uploaded file field names and whose values are source paths meaningful to you, for example {"file1":"/images/source.jpg"}. |
| `lossy` | body | `number` | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | body | `number` | no | Maximum seconds to wait for optimization before returning. |
