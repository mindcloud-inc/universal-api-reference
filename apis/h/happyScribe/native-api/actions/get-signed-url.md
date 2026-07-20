# Get Signed URL with HappyScribe

Retrieves a signed upload URL from HappyScribe.

## Endpoint

- **Method:** `GET`
- **Path:** `/uploads/new`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [Get Signed URL](https://dev.happyscribe.com/sections/product/#uploads-1-get-a-signed-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Filename and extension of the media file to upload, for example my_media.mp3. |
