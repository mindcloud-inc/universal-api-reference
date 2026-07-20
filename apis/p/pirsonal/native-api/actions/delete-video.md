# Delete Video with Pirsonal

Deletes an existing video from Pirsonal.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Delete Video](https://app.pirsonal.com/docAPI#Video_Delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoID` | body | `string` | yes | ID of the video to delete. |
| `removeFiles` | body | `boolean` | yes | Whether Pirsonal should delete external video files too, such as YouTube files. |
