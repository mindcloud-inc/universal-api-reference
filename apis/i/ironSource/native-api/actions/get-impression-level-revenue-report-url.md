# Get Impression Level Revenue Report URL with ironSource

Retrieves an impression-level revenue report URL from ironSource.

## Endpoint

- **Method:** `GET`
- **Path:** `partners/adRevenueMeasurements/v4`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Get Impression Level Revenue Report URL](https://docs.unity.com/en-us/grow/levelplay/platform/api/impression-level-revenue-server-side)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | query | `string` | no | Application key as seen on the LevelPlay platform. |
| `date` | query | `string` | no | Report date in YYYY-MM-DD format, UTC timezone. |
