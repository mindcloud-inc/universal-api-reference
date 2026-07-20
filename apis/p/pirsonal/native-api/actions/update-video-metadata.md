# Update Video Metadata with Pirsonal

Updates metadata for an existing video in Pirsonal.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Update Video Metadata](https://app.pirsonal.com/docAPI#Video_Update_Metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoID` | body | `string` | yes | ID of the video whose metadata should be updated. |
| `metaData` | body | `object` | yes | VideoMetaData_t object with updated metadata. |
