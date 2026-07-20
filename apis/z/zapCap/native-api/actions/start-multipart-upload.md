# Start Multipart Upload with ZapCap

Starts a multipart video upload in ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/upload`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Start Multipart Upload](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploadParts[]` | body | `array` | yes | Multipart part descriptors with contentLength values. |
| `filename` | body | `string` | yes | Filename to associate with the multipart upload session. |
