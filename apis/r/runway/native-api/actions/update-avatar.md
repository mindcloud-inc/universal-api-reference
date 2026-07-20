# Update Avatar with Runway

Updates an avatar in Runway.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/avatars/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Update Avatar](https://docs.dev.runwayml.com/api#tag/Avatars/paths/~1v1~1avatars~1%7Bid%7D/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the avatar to update. |
| `name` | body | `string` | no | Updated avatar name. |
| `personality` | body | `string` | no | Updated system prompt for avatar behavior. |
| `referenceImage` | body | `string` | no | Updated avatar image URL or data URI. |
| `startScript` | body | `string` | no | Optional opening message the avatar says when a session starts. |
| `voice` | body | `object` | no | Updated avatar voice object, either runway-live-preset or custom. |
