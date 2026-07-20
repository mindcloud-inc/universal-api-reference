# Create Upload Presign URL with Are.na

Creates a presigned upload URL in Are.na.

## Endpoint

- **Method:** `POST`
- **Path:** `uploads/presign`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Create Upload Presign URL](https://www.are.na/developers/explore/upload/post-presign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<object>` | yes | Array of file descriptors with filename and content_type. |
