# Create Audio Separation with CAMB.AI

Creates a new audio separation task in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/audio-separation`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Audio Separation](https://docs.camb.ai/api-reference/endpoint/create-audio-separation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_file` | body | `file` | yes | Audio file to separate into foreground and background components. |
| `project_name` | body | `string` | no | Optional project name shown in the CAMB.AI workspace. |
| `project_description` | body | `string` | no | Optional workspace description for the separation task. |
| `folder_id` | body | `number` | no | Optional CAMB.AI folder identifier for storing the task. |
