# Get Pirsonal Video Link with Pirsonal

Retrieves a downloadable Pirsonal link for a video.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Get Pirsonal Video Link](https://app.pirsonal.com/docAPI#Video_Pirsonal_Link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoID` | body | `string` | yes | ID of the video. |
| `pirsonalID` | body | `string` | yes | Pirsonal storage ID for the output file. |
