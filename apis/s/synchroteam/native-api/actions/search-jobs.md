# Search Jobs with Synchroteam

Finds jobs in Synchroteam using supported search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/Jobs/Search`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Search Jobs](https://api.synchroteam.com/v2/#search-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional. Provide the Synchroteam job search filters object (per docs). |
