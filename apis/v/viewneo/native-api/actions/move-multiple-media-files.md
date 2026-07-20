# Move Multiple Media Files with Viewneo

Moves multiple media files in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafile/move/:targetId`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Move Multiple Media Files](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.move.multiple)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `targetId` | path | `number` | yes |
| `mediaFileIds[]` | body | `array<number>` | yes |
