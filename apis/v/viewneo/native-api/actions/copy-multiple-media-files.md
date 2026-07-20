# Copy Multiple Media Files with Viewneo

Copies multiple media files in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafile/copy/:targetId`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Copy Multiple Media Files](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.copy.multiple)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `targetId` | path | `number` | yes |
| `mediaFileIds[]` | body | `array<number>` | yes |
