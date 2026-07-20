# Move Media with Wistia

Moves media to another Wistia folder or subfolder.

## Endpoint

- **Method:** `PUT`
- **Path:** `/modern/medias/move`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Move Media](https://docs.wistia.com/reference/put_medias-move)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedIds[]` | body | `array<string>` | yes |
| `projectId` | body | `string` | yes |
