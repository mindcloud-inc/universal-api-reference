# Create Video with Bookoly

Creates a new video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://bookoly.com/api/v2/generate-a-video`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Create Video](https://bookoly.com/docs/api/v2#/paths/~1generate-a-video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video` | body | `object` | yes | Video creation payload from the Bookoly v2 docs. |
| `speech` | body | `object` | no | Optional speech payload from the Bookoly v2 docs. |
| `subtitle` | body | `object` | no | Optional subtitle payload from the Bookoly v2 docs. |
| `audio` | body | `object` | no | Optional audio payload from the Bookoly v2 docs. |
