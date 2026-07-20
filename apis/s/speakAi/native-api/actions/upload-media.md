# Upload Media with Speak Ai

Creates a media file in Speak Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/upload`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Upload Media](https://docs.speakai.co/#c6106a66-6a3d-4b05-b4a2-4a68a4c1e95d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the media item. |
| `url` | body | `string` | yes | Public file URL or AWS signed URL to upload into Speak Ai. |
| `mediaType` | body | `string` | yes | Media type to upload, typically audio or video. |
| `description` | body | `string` | no | Optional description for the media item. |
| `sourceLanguage` | body | `string` | no | Optional BCP 47 language code for the media source language. |
| `tags` | body | `string` | no | Comma-separated tags for the media item. |
| `folderId` | body | `string` | no | Folder that should contain the uploaded media. |
| `callbackUrl` | body | `string` | no | Optional webhook callback URL for this upload. |
