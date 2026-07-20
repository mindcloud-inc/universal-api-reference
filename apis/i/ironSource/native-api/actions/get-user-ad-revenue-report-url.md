# Get User Ad Revenue Report URL with ironSource

Retrieves a user ad revenue report URL from ironSource.

## Endpoint

- **Method:** `GET`
- **Path:** `partners/userAdRevenue/v3`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Get User Ad Revenue Report URL](https://docs.unity.com/en-us/grow/levelplay/platform/api/impression-level-revenue-server-side)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | query | `string` | no | Application key as seen on the LevelPlay platform. |
| `date` | query | `string` | no | Report date in YYYY-MM-DD format, UTC timezone. |
| `reportType` | query | `string` | no | Report type. The current documented value is 1. |
