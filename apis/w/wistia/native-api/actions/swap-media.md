# Swap Media with Wistia

Swaps one Wistia media item with another.

## Endpoint

- **Method:** `PUT`
- **Path:** `/modern/medias/:mediaHashedId/swap`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Swap Media](https://docs.wistia.com/reference/put_medias-mediahashedid-swap)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `url` | body | `string` | no |
