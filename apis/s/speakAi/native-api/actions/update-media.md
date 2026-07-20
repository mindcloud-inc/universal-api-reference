# Update Media with Speak Ai

Updates an existing media item in Speak Ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/media/:mediaId`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Update Media](https://docs.speakai.co/#ac30a062-e214-4771-b131-afeda3b5320e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaId` | path | `string` | yes | Speak Ai media identifier. |
| `name` | body | `string` | no | Optional new media name. |
| `description` | body | `string` | no | Optional new media description. |
| `tags[]` | body | `array<string>` | no | Optional list of tags for the media item. |
