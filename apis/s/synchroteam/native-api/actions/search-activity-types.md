# Search Activity Types with Synchroteam

Finds activity types in Synchroteam using supported search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/ActivityType/Search`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Search Activity Types](https://api.synchroteam.com/v2/#search-activity-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional. Provide the Synchroteam activity type search filters object (per docs). |
