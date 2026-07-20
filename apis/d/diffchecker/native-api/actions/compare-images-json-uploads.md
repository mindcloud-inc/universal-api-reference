# Compare Images (JSON, Uploads) with Diffchecker

Compares images in Diffchecker and returns a JSON diff from uploads.

## Endpoint

- **Method:** `POST`
- **Path:** `/image`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Images (JSON, Uploads)](https://www.diffchecker.com/docs/image/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left_image` | body | `file` | yes | Left image upload. |
| `right_image` | body | `file` | yes | Right image upload. |
