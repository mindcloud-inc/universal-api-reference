# Request Video Upload Token with ChipBot

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/utility/video-upload/request`
- **Base URL:** `https://getchipbot.com`
- **Official documentation:** [Request Video Upload Token](https://getchipbot.com/api-docs/video-exp/video-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checksumMd5` | body | `string` | yes | MD5 checksum of the full video file. |
| `size` | body | `number` | yes | Video file size in bytes. |
| `data.videoExpId` | body | `string` | yes | The target video experience identifier. |
