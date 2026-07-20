# Delete Videos with Vooplayer

Deletes one or more videos from Vooplayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/deleteVideo`
- **Base URL:** `https://api.spotlightr.com`
- **Official documentation:** [Delete Videos](https://app.spotlightr.com/docs/api/#deleteVideo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IDs[]` | body | `array<number>` | yes | Array of video IDs to delete. Send multiple values as a array. |
