# Update Video with Pirsonal

Updates an existing video in your Pirsonal account.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Update Video](https://app.pirsonal.com/docAPI#Video_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoID` | body | `string` | yes | ID of the video to update. |
| `videoUpdate` | body | `object` | yes | VideoUpdate_t object with video fields to update. |
