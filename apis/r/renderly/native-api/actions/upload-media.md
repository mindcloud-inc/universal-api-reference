# Upload Media with Renderly

Creates a media upload URL in Renderly.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads`
- **Base URL:** `https://renderly.video/api/v1`
- **Official documentation:** [Upload Media](https://renderly.video/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | body | `string` | yes | MIME type of the file to upload, for example video/mp4 or image/png. |
