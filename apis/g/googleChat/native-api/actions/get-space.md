# Get Space with Google Chat

Retrieves details about a Google Chat space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:space`
- **Base URL:** `https://chat.googleapis.com/v1`
- **Official documentation:** [Get Space](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Enter only the space ID from the List Spaces result. If the result shows spaces/4Oe1TyAAAAE, enter 4Oe1TyAAAAE here. |
