# Read Discussion Comments with OneAll

Retrieves comments for a LoudVoice discussion from OneAll.

## Endpoint

- **Method:** `GET`
- **Path:** `/loudvoice/comments/<discussion_token>/comments.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Read Discussion Comments](https://docs.oneall.com/api/resources/loudvoice/discussions/comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discussion_token` | path | `string` | yes | The OneAll discussion token. |
