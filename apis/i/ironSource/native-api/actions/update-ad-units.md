# Update Ad Units with ironSource

Updates existing ad units in ironSource.

## Endpoint

- **Method:** `PUT`
- **Path:** `levelPlay/adUnits/v1/:appKey`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Update Ad Units](https://docs.unity.com/en-us/grow/levelplay/platform/api/ad-units)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adUnits` | body | `string` | no | Array of mediation ad unit objects to update. |
| `appKey` | path | `string` | no | Application key as seen on the LevelPlay platform. |
