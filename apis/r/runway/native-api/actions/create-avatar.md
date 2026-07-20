# Create Avatar with Runway

Creates an avatar in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/avatars`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Create Avatar](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Character name for the avatar. |
| `personality` | body | `string` | yes | System prompt describing how the avatar should behave. |
| `referenceImage` | body | `string` | yes | HTTPS URL, Runway URI, or data URI for the avatar image. |
| `voice` | body | `object` | yes | Voice object for the avatar, either runway-live-preset or custom. |
