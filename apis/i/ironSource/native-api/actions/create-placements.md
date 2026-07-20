# Create Placements with ironSource

Creates new placements in ironSource.

## Endpoint

- **Method:** `POST`
- **Path:** `partners/publisher/placements/v1`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Create Placements](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | body | `string` | no | Application key to create placements for. |
| `placements` | body | `string` | no | Array of placement objects to create. |
