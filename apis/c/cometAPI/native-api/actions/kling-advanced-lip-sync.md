# Kling Advanced Lip Sync with CometAPI

Creates a Kling advanced lip-sync task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/advanced-lip-sync`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Advanced Lip Sync](https://apidoc.cometapi.com/api/video/kling/counterpart-creating-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `face_choose` | body | `string` | yes | Face selection index. |
| `session_id` | body | `string` | yes | Session identifier. |
