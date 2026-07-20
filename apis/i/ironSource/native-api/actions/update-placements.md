# Update Placements with ironSource

Updates existing placements in ironSource.

## Endpoint

- **Method:** `PUT`
- **Path:** `partners/publisher/placements/v1`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Update Placements](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | body | `string` | no | Application key to update placements for. |
| `placements` | body | `string` | no | Array of placement objects to update. |
