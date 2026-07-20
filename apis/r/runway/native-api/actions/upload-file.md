# Upload File with Runway

Creates an ephemeral file upload in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/uploads`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Upload File](https://docs.dev.runwayml.com/api#tag/Uploads/paths/~1v1~1uploads/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Filename with a supported image, video, or audio extension. |
| `type` | body | `string` | yes | Upload type. Runway currently requires ephemeral. |
