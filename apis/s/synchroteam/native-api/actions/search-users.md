# Search Users with Synchroteam

Finds users in Synchroteam using supported search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/User/Search`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Search Users](https://api.synchroteam.com/v2/#search-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional. Provide the Synchroteam user search filters object (per docs). |
