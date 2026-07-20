# Search Activities with Synchroteam

Finds activities in Synchroteam using supported search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/Activities/Search`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Search Activities](https://api.synchroteam.com/v2/#search-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional. Provide the Synchroteam activity search filters object (per docs). |
