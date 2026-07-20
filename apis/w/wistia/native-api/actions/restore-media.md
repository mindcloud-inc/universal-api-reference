# Restore Media with Wistia

Restores archived media to your Wistia account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/modern/medias/restore`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Restore Media](https://docs.wistia.com/reference/put_medias-restore)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedIds[]` | body | `array<string>` | yes |
